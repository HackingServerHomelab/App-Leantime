# App-Leantime

## First Time Prerequisites

1. `rm ./Data/mysql/.gitkeep`
2. Run [Traefik](https://github.com/mattlombana/App-Traefik)

## Running the Containers

1. Update the following environment variables in [docker-compose.yml](./Docker/docker-compose.yml)
    * `MYSQL_ROOT_PASSWORD=changeme`
    * `MYSQL_PASSWORD=changeme`
    * `LEAN_DB_PASSWORD=changeme`
    * `LEAN_APP_URL=https://example.com`
2. Update the following volumes in [docker-compose.yml](./Docker/docker-compose.yml)
    * `../Data/leantime:/data`
    * `../Data/mysql:/var/lib/mysql`
3. Update the Traefik host label in [docker-compose.yml](./Docker/docker-compose.yml)
    * ``"traefik.http.routers.leantime.rule=Host(`localhost`)"``
4. Run `docker-compose -f ./Docker/docker-compose.yml up -d`

## First Time Setup

1. Visit <https://your-ip/install>
