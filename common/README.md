# Common

PostgreSQL and pgAdmin as separate stacks, connected through a shared `reverse-proxy` Docker network. pgAdmin is labeled for [Traefik](https://traefik.io/) to serve it at `pgadmin.mediusoft.com`.

## Setup

1. Create the shared network (once):

   ```sh
   docker network create reverse-proxy
   ```

2. From inside the `common/postgres` folder, start PostgreSQL:

   ```sh
   docker-compose up -d
   ```

3. From inside the `common/pgadmin` folder, start pgAdmin:

   ```sh
   docker-compose up -d
   ```

4. Open pgAdmin at <http://localhost:8080> and register the server with host name `postgres` and port `5432`.

> If the `database` stack is running, stop it first (`docker-compose down` in the `database` folder). Both use the same container names and ports.
