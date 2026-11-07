# paint2shell

Static site hosted on GitHub Pages. Everything served lives in `site/`.

## Local dev

```sh
docker compose up
```

Open http://localhost:8080. `site/` is mounted live, so just refresh after edits.

Alternatively, build a standalone image (mirrors what gets deployed):

```sh
docker build -t paint2shell .
docker run --rm -p 8080:80 paint2shell
```

## Deploy

Pushing to `main` runs `.github/workflows/pages.yml`, which publishes `site/`.
One-time setup: repo **Settings → Pages → Source: GitHub Actions**.
