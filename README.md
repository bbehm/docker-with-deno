# Docker with Deno

Trying out containerizing a Deno app with Docker. 

`docker-compose up --build`

If we omit the `--build` flag - it's using images that have previously been built to launch the container.

### Adding a database

- Using the [PostgreSQL Docker image](https://hub.docker.com/_/postgres).
- __Database migrations__: Adding [Flyway](https://flywaydb.org/) - version control for your database.

Created a `database.env` file for database credentials and added to gitignore.
