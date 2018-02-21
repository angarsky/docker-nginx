# NGINX + PageSpeed

A Docker image with NGINX and the PageSpeed module.

## Usage

The NGINX configuration is based on the official docker image - check out the ```nginx -V``` command.

Example of a ```docker-compose.yml``` file:

```
version: '2'

services:
  web:
    image: angarsky/nginx-pagespeed
    ports:
      - "80:80"
    volumes:
      - ./site:/var/www
      - ./docker/nginx/conf.d:/etc/nginx/conf.d
    container_name: web
```
