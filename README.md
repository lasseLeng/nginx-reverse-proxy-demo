# Nginx Reverse Proxy Demo (Docker)

Dieses Repository zeigt ein einfaches Setup mit **Nginx als Reverse Proxy** vor zwei separaten Web-Apps.

## Komponenten

- **reverse-proxy** – Nginx, hört auf Port 80 (nach außen weitergereicht auf 8080)
- **app1** – einfacher statischer Web-Container (Nginx mit eigener `index.html`)
- **app2** – zweiter statischer Web-Container (ebenfalls Nginx mit eigener `index.html`)

Aufrufe:

- `http://localhost:8080/` – Textantwort vom Reverse Proxy
- `http://localhost:8080/app1` – Weiterleitung zu `app1`
- `http://localhost:8080/app2` – Weiterleitung zu `app2`

## Voraussetzungen

- Docker
- Docker Compose (oder `docker compose` CLI)

## Start

```bash
docker compose up -d
# oder:
# docker-compose up -d
