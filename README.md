# Docker image - PostgreSQL with PostGIS and hstore enabled

---------------------------------------------------------

## Details

- PostgreSQL 10.1
- PostGIS 2.4.2

## Build image

    docker build -t skywidesoft/postgres-hstore-postgis .

## Push image

    docker push skywidesoft/postgres-hstore-postgis

## Tag image

    docker tag [image-id] skywidesoft/postgres-hstore-postgis:10.1_2.4.2
    docker push skywidesoft/postgres-hstore-postgis:10.1_2.4.2

## Run container

    docker run --name pg101-postgis24 -p 5432:5432 -v postgis-data:/var/lib/postgresql/data -e POSTGRES_USER=dev -e POSTGRES_PASSWORD=Password1 -d skywidesoft/postgres-hstore-postgis:10.1_2.4.2
