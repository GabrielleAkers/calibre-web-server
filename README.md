# calibre-web-server
All the files necessary to run a self hosted [calbre-web-automated](https://github.com/crocodilestick/Calibre-Web-Automated) instance with an nginx reverse proxy.

I currently run this on an ubuntu instance hosted by hetzner.

Change the file [template.env](./template.env) to `.env` and fill in the values then deploy everything to your server and run `docker compose up -d` to start the containers.