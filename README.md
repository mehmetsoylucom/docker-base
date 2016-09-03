# Docker base

```bash
docker pull ubuntu:14.04 

docker run -it -d --name web ubuntu:14.04

docker attach web

apt update

apt install -y git

cd ~

git clone http://www.github.com/mehmetsoylucom/docker-base

cd docker-base

bash base-install.sh
```

Answer mysql password questions. And exit with ctrl+d from docker container. 
  
Create a locally docker image for backup

```bash 
docker commit web base14

docker run -it -d -P --name base14 -v /var/www/codes/root:/var/www/codes/root base14
```

Use this command in host when you need docker container ip. 

```bash
docker network inspect bridge
```

Publish path is public directory in root for rails or sinatra. ( /var/www/codes/root/public in virtualhost )

Have a nice coding...
