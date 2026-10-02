# Storage

[RustFS](https://github.com/rustfs/rustfs), an S3-compatible object store, for local development. It replaces MinIO, whose community edition is archived and no longer published on Docker Hub.

## Prerequisites

- [Docker Desktop](https://www.docker.com/products/docker-desktop/)

## Setup

1. Clone the project.

2. From inside the `storage` folder, start the containers:

   ```sh
   docker-compose up -d
   ```

   The `create-bucket` container creates the `edu` bucket, makes `edu/avatars/*` and `edu/articles/*` publicly readable, and exits.

3. Open the RustFS console at <http://localhost:9001/rustfs/console/> and log in:

   | Field | Value |
   | --- | --- |
   | Access key | `rustfsadmin` |
   | Secret key | `Storage123!` |

## Connecting an app

| Setting | Value |
| --- | --- |
| S3 endpoint | `http://localhost:9000` (path-style URLs) |
| Region | `us-east-1` |
| Bucket | `edu` |
| Access key / secret key | `rustfsadmin` / `Storage123!` |
| Public file URL | `http://localhost:9000/edu/<key>` |

## Data

Objects are stored in `../../storage-data` on the host (the `storage-data` folder next to `stack`), so they persist across container restarts.

## Stop

```sh
docker-compose down
```
