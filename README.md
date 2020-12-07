# Docker with Deno

Trying out containerizing a Deno app with Docker. 

Clone and run `docker-compose up --build` - you need to create a `database.env` file with database credentials.

If we omit the `--build` flag - it's using images that have previously been built to launch the container.

### Adding a database

- Using the [PostgreSQL Docker image](https://hub.docker.com/_/postgres).
- __Database migrations__: Adding [Flyway](https://flywaydb.org/) - version control for your database.

Created a `database.env` file for database credentials and added to gitignore - looks like:

```
PGPORT=5432
PGDATABASE=database
PGUSER=username
PGPASSWORD=password
PGHOST=postgres-database

POSTGRES_USER=username
POSTGRES_PASSWORD=password
POSTGRES_DB=database

FLYWAY_USER=username
FLYWAY_PASSWORD=password
FLYWAY_URL=jdbc:postgresql://postgres-database:5432/database
```

