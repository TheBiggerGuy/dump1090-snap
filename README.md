# Dump1090 Snap
A dump1090 server running via the Snap package system. This will run a dump1090 server for local only connections ready to be used by other apps such as fr24feed. 

# Ussage

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
```bash
nc 127.0.0.1 30003
```
