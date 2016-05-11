## Nginx Dockerfile


This repository contains [Nginx](http://nginx.org/) for [Docker](https://www.docker.com/)'s [automated build](https://registry.hub.docker.com/u/lucianojr/nginx/) published to the public [Docker Hub Registry](https://registry.hub.docker.com/).


### Base Docker Image

* [luciano-jr/ubuntu](https://github.com/luciano-jr/ubuntu)


### Installation

1. Install [Docker](https://www.docker.com/).

2. Download [automated build](https://registry.hub.docker.com/u/lucianojr/nginx/) from public [Docker Hub Registry](https://registry.hub.docker.com/): `docker pull lucianojr/nginx`

   (alternatively, you can build an image from Dockerfile: `docker build -t="lucianojr/nginx" github.com/luciano-jr/nginx`)


### Usage

    docker run -d -p 80:80 lucianojr/nginx

#### Attach persistent/shared directories

    docker run -d -p 80:80 -v <sites-enabled-dir>:/etc/nginx/conf.d -v <certs-dir>:/etc/nginx/certs -v <log-dir>:/var/log/nginx -v <html-dir>:/var/www lucianojr/nginx

After few seconds, open `http://<host>` to see the welcome page.
