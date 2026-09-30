# Stack

Docker Compose setups for local development tools.

| Folder | Description |
| --- | --- |
| [`database/`](database/README.md) | PostgreSQL + pgAdmin for local development |
| [`common/`](common/README.md) | PostgreSQL and pgAdmin as separate stacks behind a Traefik reverse proxy |

> Both setups use the same container names (`postgres`, `pgadmin`) and ports (`5432`, `8080`). Run only one at a time.

See the README inside each folder for setup instructions.
