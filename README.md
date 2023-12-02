# home-automation

Dieses Repository enthält die Konfiguration sowie Anweisungen zum Erstellen eines Software-Stacks bestehend aus:
- NodeRED
- InfluxDB
- Grafana
- Mosquitto
- Portainer
- Traefik

Die Konfiguration ist auf den Betrieb auf einem Raspberry Pi 4 ausgelegt. Sie basiert auf dem Repository https://github.com/SensorsIot/IOTstack.

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
