# iocage-my-plugins
Plugin manifest files for iocage.

## Prerequisites
A \*BSD system with the iocage jailmanager.

## Installing Plugins
Download a plugin manifest file to your local file system.
```
fetch https://raw.githubusercontent.com/dlcisme/iocage-my-plugins/master/mineos.json
```
Install the plugin using static IP or DHCP.

* Using static IP.  Adjust host interface and IP address as needed.
```
iocage fetch -P -n mineos.json ip4_addr="re0|192.168.0.100"
```
* Using DHCP.
```
iocage fetch -P -n dockett.json vnet=on dhcp=on bpf=yes
```

## Plugin manifest files
### mineos.json
This will install [MineOS](https://minecraft.codeemo.com/mineoswiki/index.php?title=MineOS-node_(pkg_add)), an easy way to create, host and manage Minecraft servers via a Web-based User Interface.
#### NOTE: If moving servers don't forget to copy the mineos.conf file.  Location should be /etc/mineos.conf.

**mineos.conf** file should look like:
```
use_https = false
socket_host = '0.0.0.0'
#socket_port = 8443
#base_directory = '/var/games/minecraft'
socket_port = 8080
base_directory = '/app-data/minecraft'

ssl_private_key = '/etc/ssl/certs/mineos.key'
ssl_certificate = '/etc/ssl/certs/mineos.crt'
ssl_cert_chain = ''

webui_locale = 'en_US'
additional_logfiles = ''
optional_columns = ''
```

### lidarr.json
This will install [Lidarr](https://github.com/Lidarr/Lidarr), a music collection manager for Usenet and BitTorrent users.

### jackett.json
This will install [Jackett](https://github.com/Jackett/Jackett), a proxy server: it translates queries from apps (Sonarr, Radarr, SickRage, CouchPotato, Mylar, etc) into tracker-site-specific http queries.

### nginx.json
This will install [Nginx](https://nginx.com), a web server which can also be used as a reverse proxy, load balancer, mail proxy and HTTP cache.

### tautulli.json
This will install [Tautulli](https://github.com/Tautulli/Tautulli), an application for monitoring, analytics and notifications for Plex Media Server.

### urbackup.json
This will install [UrBackup](https://www.urbackup.org) server, a client/server backup system. 

### dockett.json
This will install a server that will allow you to backup files using an rsync script (also included).

### overviewer.json
This will install [Overviewer](https://overviewer.org), a command-line tool for rendering high-resolution maps of Minecraft worlds. It generates a set of static html and image files and uses Leaflet to display a nice interactive map.
