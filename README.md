# calibre-web-server
All the files necessary to run a self hosted [calbre-web-automated](https://github.com/crocodilestick/Calibre-Web-Automated) instance with an nginx reverse proxy.

I currently run this on an ubuntu instance hosted by hetzner.

## To deploy
1. Clone the repo
2. Generate an ssl cert, i use certbot like this:
```
sudo snap install --classic certbot
sudo ln -s /snap/bin/certbot /usr/bin/certbot
sudo certbot certonly --nginx
sudo certbot renew --dry-run
```
The cert and key you are interested will be whatever files the symlinks `fullchain.pem` and `privkey.pem` point to under `/etc/letsencrypt/live/<your domain>`

3. Modify the [502 page](./nginx/public/502.html) to your liking.
4. Rename the file [template.env](./template.env) to `.env` and fill in the values
5. Run `docker compose up -d` to start the containers.