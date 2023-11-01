# basicstation

### Docker instalation:
```bash
wget -O get-docker.sh https://get.docker.com
sudo sh get-docker.sh
sudo usermod -aG docker ${USER}
newgrp docker
sudo systemctl enable docker
```

### Configuration:
GatewayEUI: file config/station.conf, field station_conf.routerid  
Server address: file config/tc.uri

### Run Container:
```bash
docker compose up
```
