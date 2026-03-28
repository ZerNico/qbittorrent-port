# Port - Docker mod for qBittorrent

This mod adds a script that automatically retrieves the forwarded port from Gluetun and configures it as the incoming port in [qBittorrent](https://github.com/linuxserver/docker-qbittorrent).

## Requirements
- The qBittorrent container uses gluetun as the network provider.
- Port forwarding is enabled in Gluetun.

## Setup
1. Add `DOCKER_MODS=ghcr.io/zernico/qbittorrent-port:latest` to your qBittorrent Docker environment variables.

2. Make sure gluetun is running and has successfully forwarded a port.

3. The script will automatically configure the incoming port in qBittorrent.

## Environment Variables

| Variable | Default | Description |
| --- | --- | --- |
| `QBIT_HOST` | `localhost` | qBittorrent WebUI host |
| `QBIT_PORT` | `8080` | qBittorrent WebUI port |
| `QBIT_USER` | `admin` | qBittorrent WebUI username |
| `QBIT_PASS` | `adminadmin` | qBittorrent WebUI password |
