### Traefik2 + docker + laravel example

Very simple script to example with Traefik v2, docker and laravel project, (dev enviroment)

dependences:
    - docker
    - laravel

testing with laravel 8.18.1 (php 8) 

Settings:

Create .env file:

cp env.example .env

edit your file .env
    - HOST: "set host you want to use (default laravel.vm)"
    - PROJECT_FOLDER:  "laravel folder (default laravel)"
 
building docker images:

docker-compose build

start:

docker-compose up -d

enter in php container with bash:

docker exec -it php /bin/bash

install laravel (in php container):

composer create-project laravel/laravel .


dont forget setting the localhost your hosts file (linux,mac):
    sudo vi /etc/hosts  (add in new line: 127.0.0.1   laravel.vm)

if want use mysql in laravel, set file .env in laravel folder (example):

DB_CONNECTION=mysql
DB_HOST=mysql
DB_PORT=3306
DB_DATABASE=homestead
DB_USERNAME=homestead
DB_PASSWORD=secret

---

good luck