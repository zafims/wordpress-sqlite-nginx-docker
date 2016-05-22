## Wordpress on Nginx using Sqlite instead of MySQL Dockerfile

This repository contains **Dockerfile** of Wordpress on Nginx using Sqlite instead of MySQL

### Base Docker Image

* Nginx Official build for Docker (https://registry.hub.docker.com/_/nginx/)

### Usage

    mkdir -p /var/wordpress/database /var/wordpress/uploads    
    docker run -d -p 3000:80 -v /var/wordpress/database:/var/wordpress/database -v /var/wordpress/uploads:/usr/share/nginx/html/wp-content/uploads zenozeng/wordpress-sqlite-nginx-docker    

After few seconds, open `http://<host>` to see the wordpress install page.

### Build from Dockerfile

    docker build -t="zenozeng/wordpress-sqlite-nginx-docker" github.com/zenozeng/wordpress-sqlite-nginx-docker
