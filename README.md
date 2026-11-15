# Mathixel Alpine Edition

A pixel-picture arithmetic game based on [davidmarek/mathogram](https://github.com/davidmarek/mathogram), with addition/subtraction and multiplication modes.

- Switch modes at the top of the page.
- Multiplication covers every pair from **1 × 1 through 10 × 10**, with answers up to **100**.
- Correct answers reveal pixels automatically. Each mode saves its own progress in your browser.
- English and Czech interfaces, offline support, and light/dark themes.

## Play online

[Open Mathixel Alpine Edition](https://mathixel-alpine.zilka.me/)

## Run locally

Install Docker and Docker Compose, then run:

```sh
docker compose up --build -d
```

Open http://localhost:4173. The port is available only on your computer.

All dependency installation, lint, tests, and builds run inside Docker. The serving container contains only the compiled site and nginx.

## Publish

Push to `main` to run the GitHub Pages workflow. It tests and builds inside Docker, then deploys the static output to GitHub Pages. Set **Settings → Pages → Source** to **GitHub Actions**.

The app uses relative asset paths so it works under `/mathixel-alpine-edition/`. No custom domain or backend is required.

## Credits

Original game, artwork, and content: [davidmarek/mathogram](https://github.com/davidmarek/mathogram), downloaded at commit `082c148`. See [the upstream documentation](docs/upstream-readme.md) for the original game design and background. This edition adds independent multiplication progress and the full 1–10 multiplication table.
