# Configure X-Pack Security for ssl

## 1. stop kibana

    sudo systemctl stop kibana


## 2. Generate ssl Certificate and key

    cd /usr/share/elasticsearch/bin
    sudo ./elasticsearch-certutil ca --pem

## 3. Adding Path of certificate and key in kibana.yml

unzip elastic-stack-ca.zip

mv ca /

sudo nano /etc/kibana/kibana.yml

server.ssl.enabled : true
server.ssl.certificate : /ca/ca.crt
server.ssl.key : /ca/ca.key

sudo systemctl start kibana
