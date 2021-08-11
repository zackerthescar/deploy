# deploy
The docker-compose files I use to set up the services I host. 

**SWAG**: Secure Web Application Gateway. Essentially [LinuxServer.io's highly customizable NGINX docker image](https://docs.linuxserver.io/general/swag) perfect for reverse proxy use.

**Git**: A modification version of [Anne](https://gitlab.boonchuy.com/anne/)'s [Gitea-Drone](https://gitlab.boonchuy.com/anne/deploy/-/tree/master/Gitea-Drone) deploy files. You should probably check out her version.

**Media**: My self-hosted media stack, with Jellyfin as the media player, [Radarr](https://sonarr.tv/) as the TV shows manager, and [Transmission](https://transmissionbt.com/) as the torrent client. Note: for legal reason I can't condone using Radarr and Transmission, hence why they are in separate folders.

**Cloudflare-ddns**: A pretty cool docker image that is essentially a cron-job that uses the Cloudflare API to update your DNS records.
