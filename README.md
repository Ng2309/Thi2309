# Thi2309
Nano
mkdir nano && cd nano
version: '3'
services:
  monitor:
    image: "nanotools/nanonodemonitor:TAG"
    restart: "unless-stopped"
    ports:
     - "80:80"
    volumes:
     - "~:/opt"
  node:
    image: "nanocurrency/nano:TAG"
    restart: "unless-stopped"
    ports:
     - "7075:7075"
     - "127.0.0.1:7076:7076"
    volumes:
     - "~:/root"
sudo docker-compose up -d
cd ~/nanoNodeMonitor
nano_node_1
