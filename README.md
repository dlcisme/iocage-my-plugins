# iocage-my-plugins
Plugin manifest files for iocage.

## Prerequisites
A \*BSD system with the iocage jailmanager.

## Installing Plugins
Download a plugin manifest file to your local file system.
```
fetch https://raw.githubusercontent.com/dlcisme/iocage-my-plugins/master/mineos.json
```
Install the plugin.  Adjust host interface and IP address as needed.
```
iocage fetch -P -n mineos.json ip4_addr="em0|192.168.0.100"
```

## Plugin manifest files
### mineos.json
This will install [MineOS](https://minecraft.codeemo.com/mineoswiki/index.php?title=MineOS-node_(pkg_add)), an easy way to create, host and manage Minecraft servers via a Web-based User Interface.

### lidarr.json
This will install [Lidarr](https://github.com/lidarr/Lidarr), a music collection manager for Usenet and BitTorrent users.
