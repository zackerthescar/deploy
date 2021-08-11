# Media
These are the services I use for my media setup at home.

Transmission is my torrent client, Jackett is my torrent indexer, and Sonarr is used to manage my collection of TV shows. I personally don't use Radarr, Lidarr, or the other media managers, as those are generally easy enough for me to manage manually.

I use Jellyfin as my media server, as I refuse to pay the Plex Pass for the hardware transcoding feature, which I need because my collection has a variety of codecs. However, the Jellyfin `docker-compose` is separate from the Transmission, Jackett, and Sonarr one, allowing one to easy move between media servers as desired. 

# environment.txt
As the media server itself and the media management tools are on different `docker-compose` files, I found it easier to have a single environment file governing the two. However, special precaution must be taken. 

Before starting either services, create a symlink between the environment.txt file provided into the `./jellyfin` **and** `./torrent` folder, and edit `environment.txt` with the approrpriate values for your setup.

For Jellyfin:
```
$ cd jellyfin
$ ln -s ../environment.txt .env
```
For torrent:
```
$ cd torrent
$ ln -s ../environment.txt .env
```

| Variable | Description |
|--|--|
| DLDIR | Your downloads directory |
| TVDIR | Your TV Shows directory |
| MOVIESDIR | Your Movies directory |
| MUSICDIR | Your Music directory
| PUID | Your User PUID |
| PGID | Your User PGID |
| TZ | Your timezone
| NETWORK | The network your reverse proxy resides on. |

# Credits


[@PARC6502](https://github.com/PARC6502): Their [docker-media-server](https://github.com/PARC6502/docker-media-server) `docker-compose` file serves as the inspiration of mine. I've used this `docker-compose` file before I created this newer one.

