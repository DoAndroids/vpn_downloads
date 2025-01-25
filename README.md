
# VPN Downloads

# Instructions
Download the repo to a directory for a start

## Choice of VPN type
There are two docker-compose files here. Choose either the OpenVPN or Wireguard version.
Rename it to "docker-compose.yml", then remove the other one.

## Configuring
Edit the .env file and change the appropriate settings:
* PIA_USER: this is your Private Internet Access username
* PIA_PASS: your Private Internet Access password
* PIA_REGION: if using the OpenVPN protocol, this should be set using on the 'name' values from [here] (https://serverlist.piaservers.net/vpninfo/servers/v6). e.g. "UK London"
* PIA_REGION_WG: if using the Wireguard protocol, this should be set using one of the 'id' values from [here](https://serverlist.piaservers.net/vpninfo/servers/v6). e.g. "uk"
* TZ: choose the timezone you want the containers to use
* PUID: this is the Unix user ID of the system user the containers will run as
* PGID: this is the Unix group ID of the system user the containers will run as
* QBT_WEBUI_PORT: the port that the qBittorrent client will be accessed via
* QBT_USER: your qBittorrent user (used for the port forwarding update)
* QBT_PASS: your qBittorent password (used for the port forwarding update)
* NETWORK_SUBNET: this should be the machine's local IP address, with a zero at the end rather than whatever is assigned

# Running
In the directory where your files are, then run:

```docker-compose up -d```

You can then check them using:

```docker-compose ps```

## Configuring

# Other software
All configuration files should be in the "./config" directory (below where your docker-compose.yml file is.

## Accessing
You should be able to access using the local IP address and the services's port.
e.g. http://localhost:7474 for autobrr
