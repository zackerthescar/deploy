# SWAG
[LinuxServer.io](https://www.linuxserver.io/)'s [SWAG](https://hub.docker.com/r/linuxserver/swag) integrates Let's Encrypt, fail2ban, and NGINX into a simple docker image, and includes reverse proxy templates for many self-hosted web applications. 

My custom `docker-compose.yml` sets up SWAG with Cloudflare DNS and wildcard subdomain certificates. This makes self-hosting applications as easy as starting up the container with a bridge network connecting it and a container configured by this `docker-compose` file, and applying a reverse-proxy template.

#
**.env**
| Variable | Description |
|--|--|
| PUID | Non-root user PUID to access container configuration files |
| PGID | Non-root user PGID to access container configuration files |
| TIMEZONE | Your local timezone |
| NETWORK | The name of the network all your web-facing containers will connect to |
| URL | Your domain name

#
**Post startup configuration**

After first startup, bring down the container.  
Create a Cloudflare API token with the **Zone:DNS Edit** permission for the zone with your domain. 
Navigate to `./config/dns-conf/` and edit `cloudflare.ini` with your API token key.
Your website will be ready-to-go on container re-start.

Visit [LinuxServer.io's SWAG](https://docs.linuxserver.io/general/swag)'s documentation for more information on configuring SWAG.
