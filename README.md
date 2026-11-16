# My Site

A lightweight, hardened static HTML site template served by Nginx in Docker.

## Structure

- `public/` contains the website assets (`index.html`, `styles.css`, `app.js`, `favicon.svg`).
- `Dockerfile` builds the Nginx Alpine image with health checks and safe file permissions.
- `docker-compose.yml` runs the container with read-only root filesystem hardening and log rotation.
- `nginx.conf` configures gzip compression, HTTP security headers, asset caching, `/health` checks, and SPA fallback routing.
- `.env.example` provides optional environment variables such as `HOST_PORT`.

## Run locally

```bash
docker compose up -d --build
```

Open `http://localhost:8080` in your browser, or verify the health endpoint at `http://localhost:8080/health`.

## Customise port

Copy `.env.example` to `.env` and change `HOST_PORT` if port `8080` is already in use:

```bash
cp .env.example .env
```

## Stop locally

```bash
docker compose down
```

## Customise content

Edit the files inside `public/`, then rebuild the image:

```bash
docker compose up -d --build
```
