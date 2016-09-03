# Docker base

```bash
docker pull ubuntu:14.04 

docker run -it -d --name web ubuntu:14.04

apt update

apt install git

cd ~

git clone http://www.github.com/mehmetsoylucom/docker-base

cd docker-base

bash base-install.sh
```

Answer mysql password questions. And exit with ctrl+d from docker container. 

```bash 
mkdir /var/www/codes
mkdir /var/www/codes/root
```

Create a locally docker image for backup

```bash 
docker commit web base14

docker run -it -d -P --name base14 -v /var/www/codes/root:/var/www/codes/root base14
```

Don't commit your host repository files to the git remote repository after work.

Have a nice coding...
