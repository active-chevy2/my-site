# My Site

A reusable static HTML site template served by Nginx in Docker.

## Structure

- `public/` contains the website files.
- `Dockerfile` builds the Nginx image.
- `docker-compose.yml` runs the site on host port `8080`.
- `nginx.conf` configures static files and single-page-app fallback routing.

## Run locally

```bash
docker compose up -d --build
```

Open `http://localhost:8080` in your browser.

## Stop locally

```bash
docker compose down
```

## Customize

Replace or edit the files inside `public/`, then rebuild the image:

```bash
docker compose up -d --build
```
