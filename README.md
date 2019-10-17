# Docker compose file for Laravel setup with pre-installed Adminer

Docker compose file with required configurations for PHP full stack or Laravel setup with PHP-fpm 7.3, Postgres 10,  Nginx web server

## Application setup steps
1. Copy or Clone your app inside "application" folder
2. Update "template.conf" inside "conf.d" folder with the below steps
a. If you want to use "HTTP" or "HTTPS" use the respective block and delete the other one
b. Replace "app.domain.com" with your domain like "www.google.com"
c. Replace "my-app" with your application folder name which you have copied or cloned inside the "application" folder in step 1.
d. Replace "app-name" with your application name "myapplication"

## /etc/hosts file in your host machine in Ubuntu
please add the below lines to your "/etc/hosts" file in your host machine

172.16.238.10 local.adminer.com

172.16.238.10 **your domain here like www.google.com**

172.16.238.12 dev-dbserver

## SSL certificates
1. If you are usign ssl please copy your cerficate to "conf.d/ssl/ssl.crt" file and copy your key to "conf.d/ssl/ssl.key" files respectively

Now do "docker-compose up -d" in the base folder
use "docker exec -it dev-phpserver bash" to login to php container bash
use "docker exec -it dev-dbserver bash" to login to DB container bash
use "docker exec -it dev-nginxserver bash" to login to nginx container bash

