# js-fastify-blog in Docker

Study project for packaging `js-fastify-blog` into Docker and configuring `docker-compose` for local development, tests, and CI/CD.

## Requirements

- Docker
- Docker Compose

## Run app

```bash
docker compose up --build app
```

The application will be available at `http://localhost:8080`.

## Run tests

```bash
docker compose up --build app-test
```

## Services

- `db` - PostgreSQL 16
- `app` - Fastify application
- `app-test` - test runner container

## CI/CD

GitHub Actions is configured to:

- run `lint` and `test`
- build and publish a Docker image on pushes to `main`

Add these repository secrets before publishing to Docker Hub:

- `DOCKERHUB_USERNAME`
- `DOCKERHUB_TOKEN`

Published image name:

```text
antoha2005/antoha2005
```

Docker Hub page:

[https://hub.docker.com/r/antoha2005/antoha2005](https://hub.docker.com/r/antoha2005/antoha2005)

