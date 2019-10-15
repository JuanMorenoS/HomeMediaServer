# HomeMediaServer

## How to install

### Prerequisites:
 - Docker
 - Docker compose

### Run it!

- Clone or Download this repo
- Go to the repo folder
- Run this command: ```docker-compose up```
- Go to the plex (http://localhost:32400) and configure your server
#### Configure Radarr and Sonarr
##### Indexer
    - Open the service
    - Go to Settings/indexers
    - Click on add/Torznab/Custom
    - Full url with: http://10.5.0.2:9117/api/v2.0/indexers/all/results/torznab/
    - Open Jacket and copy the API key
    - Put this basic Categories: 5000,5020,5030,5040,5050,5060
    - and save
##### DownloadClient
    - Go to Settings/Download Client
    - Host: 10.5.0.4
    - Port: 8080
    - User: admin
    - password: adminadmin (You can change this password in the web ui)
    - Category: tv-sonarr
    - and save

## Used ports by service:

### PLEX:
    - 32400:32400/tcp
    - 3005:3005/tcp
    - 8324:8324/tcp
    - 32469:32469/tcp
    - 1900:1900/udp
    - 32410:32410/udp
    - 32412:32412/udp
    - 32413:32413/udp
    - 32414:32414/udp
### Bazarr
    - 6767:6767
### Radarr
    - 7878:7878
### QBitTorrent
    - 8080:8080
### Sonarr
    - 8989:8989
### Jacket
    - 9117:9117


## TODO:

- [ ] Make a very simple README
- [ ] Change the qbittorrent port
- [ ] Make a description of the project
- [ ] Autoconfig all environment