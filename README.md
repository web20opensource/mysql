## MySQL Dockerfile


This repository contains **Dockerfile** of [MySQL](http://dev.mysql.com/) for [Docker](https://www.docker.com/)'s [automated build](https://registry.hub.docker.com/u/dockerfile/mysql/) published to the public [Docker Hub Registry](https://registry.hub.docker.com/).


### Base Docker Image

* [debian:stable]


### Installation

1. Install [Docker](https://www.docker.com/).

2. Download this Dockerfile into a directory named as you desire
    mkdir mysql; cd mysql; wget https://raw.githubusercontent.com/web20opensource/mysql/master/Dockerfile
3. build
    docker build - < Dockerfile
    


### Usage

#### Run `mysqld-safe`

    docker run -d --name mysql -p 3306:3306 dockerfile/mysql

#### Run `mysql`

    docker run -it --rm --link mysql:mysql dockerfile/mysql bash -c 'mysql -h $MYSQL_PORT_3306_TCP_ADDR'
