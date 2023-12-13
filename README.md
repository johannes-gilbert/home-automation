# home-automation

This repository contains the configuration and instructions to create a software stack that consists of:
- NodeRED
- InfluxDB
- Grafana
- Mosquitto
- Portainer
- Traefik

The configuration is intended to run on a Raspberry Pi 4. It bases on the [IOTstack](https://github.com/SensorsIot/IOTstack).

## Installation
For a visual installation instruction you might want to watch [#295 Raspberry Pi Server based on Docker, with VPN, Dropbox backup, Influx, Grafana, etc: IOTstack](https://www.youtube.com/watch?v=a6mjt8tWUws) (YouTube) starting at minute 7:30.
1) Clone the git-repository IOTstack: `git clone https://github.com/SensorsIot/IOTstack.git
2) `cd IOTstack`
3) Start the menu: `./menu.sh`
4) Go to `Build Stack`.
5) Select `grafana`, `influxdb`, `mosquitto`, `nodered`, `portainer-ce` and `portainer-agent`. You might need to revise the options for some of these containers.
6) Press `Enter` to build the stack.
7) In the menu go to `Miscellaneous Commands`. Select `Set swapiness to 0` as well as `Install log2ram`.

Although you could go with the [docker-compose.yml](https://github.com/johannes-gilbert/home-automation/blob/main/docker-compose.yml) provided in this repository, it eases the operation of you Raspberry Pi to go via IOTstack. IOTstack bring a bunch of utilities which help you keeping your installation up to date.

## Structure of this repo
```txt
~/
├── docker-compose.yml 
└── /volumes
    ├── grafana
    │   ├── data  
    │   └── log
    ├── influxdb
    │   └── data 
    ├── letsencrypt
    │   └── acme.json   (chmod 600)
    ├── mosquitto
    │   ├── config
    │   ├── data
    │   ├── log
    │   └── pwfile
    ├── nodered
    │   ├── data
    │   └── ssh
    └── portainer-ce
        └── data
```
