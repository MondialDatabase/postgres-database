# Mondial Database Server

An Database Server for the [Mondial Database](https://www.dbis.informatik.uni-goettingen.de/Mondial/).

It is running on PostgreSQL (11.x).

## Running the Database Server 

1. Install Docker CE.
2. Change into the project directory.
3. Run `sh build-db.sh` to build the Mondial database schema.
   NOTE: This will not do a clean rebuild of the database. If this is desired (e.g. due to a schema change), execute
   an `docker volume rm mondial-database-data` command first.
4. Run `docker-compose -p mondial up --build` to start the web services.

To shut down the web services, run `docker-compose -p mondial down`.

## Connecting to the Database Server

The Database Server will be available on `localhost:5432`. The username and database name is `postgres`.
