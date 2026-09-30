# Database

PostgreSQL and pgAdmin running together for local development.

## Prerequisites

- [Docker Desktop](https://www.docker.com/products/docker-desktop/)

## Setup

1. Clone the project.

2. From inside the `database` folder, start the containers:

   ```sh
   docker-compose up -d
   ```

3. Open pgAdmin at <http://localhost:8080> and log in:

   | Field | Value |
   | --- | --- |
   | Email | `pgadminuser@gmail.com` |
   | Password | `Database123!` |

4. Register the server in pgAdmin (**Object → Register → Server**, *Connection* tab):

   | Field | Value |
   | --- | --- |
   | Host name | `postgres-db` (the service name in `docker-compose.yml`) |
   | Port | `5432` |
   | Username | `postgres` |
   | Password | `Database123!` |

## Data

Database files are stored in `../../postgres-data` on the host (the `postgres-data` folder next to `stack`), so they persist across container restarts.

## Stop

```sh
docker-compose down
```
