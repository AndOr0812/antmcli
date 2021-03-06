# Tiny CLI tool for remote monitoring and controlling your Antminer S9

It uses Antminer firmware [cgi API endpoints](https://github.com/bitmaintech/Antminer_firmware/tree/master/sources/meta-antminer/recipes-bitmianer/lighttpd/lighttpd-1.0/www/cgi-bin)

## Dependencies

    * curl 
    * jq
    
## Installing

```
sudo curl https://raw.githubusercontent.com/pavelsr/antmcli/master/amcli -o /usr/local/bin/amcli
sudo chmod +x /usr/local/bin/amcli
```

## Using

Don't forget to change (e.g. with `sudo nano /usr/local/bin/amcli`) following enviroment variables (below are defaults):

```
MINER_IP=192.168.0.105
USER=root
PASS=root
```

Available options:

```
Usage: ./amcli [-h] [-v] [-r] [-l]
  -h  Help. Display this message and quit
  -v  Version. Print version number and quit
  -a  Show Antminer API authorization details
  -r  Reboot Antminer
  -l  Show Antminer linux kernel log

Without any option specified it's showing json dashboard
```

## Minimal bash version required

Tested on bash 4.3.48