Docker image - PostgreSQL with PostGIS and hstore enabled
---------------------------------------------------------

### Details
- PostgreSQL 9.6.3
- PostGIS 2.3.2

### Build image
    docker build -t skywidesoft/postgres-hstore-postgis .

### Push image
    docker push skywidesoft/postgres-hstore-postgis

### Tag image
    docker tag [image-id] skywidesoft/postgres-hstore-postgis:9.6.3_2.3.2
    docker push skywidesoft/postgres-hstore-postgis:9.6.3_2.3.2

### Run container
    docker run --name pg96-postgis23 -p 5432:5432 -v postgis-data:/var/lib/postgresql/data -e POSTGRES_USER=dev -e POSTGRES_PASSWORD=Password1 -d skywidesoft/postgres-hstore-postgis:9.6.3_2.3.2
