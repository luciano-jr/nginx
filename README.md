## Nginx Dockerfile


This repository contains **Dockerfile** of [Nginx](http://nginx.org/) for [Docker](https://www.docker.com/)'s [automated build](https://registry.hub.docker.com/u/luciano-jr/nginx/) published to the public [Docker Hub Registry](https://registry.hub.docker.com/).


### Base Docker Image

* [luciano-jr/ubuntu](https://github.com/luciano-jr/ubuntu)


### Installation

1. Install [Docker](https://www.docker.com/).

2. Download [automated build](https://registry.hub.docker.com/u/luciano-jr/nginx/) from public [Docker Hub Registry](https://registry.hub.docker.com/): `docker pull luciano-jr/nginx`

   (alternatively, you can build an image from Dockerfile: `docker build -t="luciano-jr/nginx" github.com/luciano-jr/nginx`)


### Usage

    docker run -d -p 80:80 luciano-jr/nginx

#### Attach persistent/shared directories

    docker run -d -p 80:80 -v <sites-enabled-dir>:/etc/nginx/conf.d -v <certs-dir>:/etc/nginx/certs -v <log-dir>:/var/log/nginx -v <html-dir>:/var/www luciano-jr/nginx

After few seconds, open `http://<host>` to see the welcome page.
