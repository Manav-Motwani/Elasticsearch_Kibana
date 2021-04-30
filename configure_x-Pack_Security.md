# Configure X-Pack Security 

## 1. stop kibana

    sudo systemctl stop kibana

## 2. Stop elasticsearch 

    sudo systemctl stop elasticsearch

## 3. enable xpack in elasticsearch.yml

    sudo nano /etc/elasticsearch/elasticsearch.yml
    xpack.security.enabled: true

## 4. Setup default user passwords

    cd /usr/share/elasticsearch/bin
    sudo ./elasticsearch-setup-passwords auto


## System Passwwords 

Changed password for user apm_system
PASSWORD apm_system = JemiK9L5LmQGClxFhCID

Changed password for user kibana_system
PASSWORD kibana_system = Hrpxy7Zi595TN0ResDu0

Changed password for user kibana
PASSWORD kibana = Hrpxy7Zi595TN0ResDu0

Changed password for user logstash_system
PASSWORD logstash_system = XpEiTzfdb6ERydaxMeWe

Changed password for user beats_system
PASSWORD beats_system = PWdGDIQbT8mFpwsLEpRI

Changed password for user remote_monitoring_user
PASSWORD remote_monitoring_user = mANAh62R544JcKokFfOg

Changed password for user elastic
PASSWORD elastic = 3yUm3epwNurHX0ycTiGk


## 5. Add the default username in kibana

sudo nano /etc/kibana/kibana.yml

change default username and password

elasticsearch.username: "kibana"
elasticsearch.password: "new_password"



