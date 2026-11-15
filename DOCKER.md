# Run locally with Docker

The source was downloaded from davidmarek/mathogram at commit 082c148.

From this directory, run:

```sh
sudo docker compose up --build -d
```

Open http://localhost:4173. The port is bound only to this computer.
Docker builds the app with Node 24 and serves the production build with nginx.
Game progress is saved in your browser.

Check status or stop the app:

```sh
sudo docker compose ps
sudo docker compose down
```
