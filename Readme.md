# docker-dns 

## install docker
```sh
sudo apt update
sudo apt install -y apt-transport-https ca-certificates curl software-properties-common
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable"
sudo apt update
sudo apt install -y docker-ce
```

## create nginx network
```sh
sudo docker network create nginx-network
```

## Chmod 700
```sh
chmod 700 duckdns.sh
```
## Set up cron job
```sh
crontab -e
```
<hr>*/5 * * * * ~/duckdns/duckdns.sh >/dev/null 2>&1

## install nginx by Docker

```sh
cd ~/nginx
sudo docker-compose up -d
```






