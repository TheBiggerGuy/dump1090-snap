# Dump1090 Snap

[![Snap Status](https://build.snapcraft.io/badge/TheBiggerGuy/dump1090-snap.svg)](https://build.snapcraft.io/user/TheBiggerGuy/dump1090-snap)

A dump1090 server running via the Snap package system. This will run a dump1090 server for local only connections ready to be used by other apps such as [fr24feed](https://github.com/TheBiggerGuy/fr24feed-snap). 

# Usage

## Install
```bash
sudo snap install dump1090-net
sudo snap connect dump1090-net:raw-usb 
```

## Update
```bash
sudo snap refresh dump1090-net
```

## View Logs
```bash
sudo journalctl -u snap.dump1090-net.dump1090.service
```

## Test
### Run Interactive
```bash
sudo snap run dump1090-net.dump1090-interactive
```
### Connect to Server
#### AVR
```bash
nc 127.0.0.1 30003
```
#### Beast
```bash
nc 127.0.0.1 30005 | xxd -p
```
