# dockerwp-isolate
Simple Wordpress with lemp isolated stack build in Docker.
=======
# Wordpress LEMP Stack Isolation with Docker Compose

Simple stack using 4 Containers on Docker, this compose file runs a isolated container for NGINX, Wordpress with PHP-FPM, MySQL and Certibot SSL Install/Validation.

## Getting Started

For running this, basically you need to clone this repo and create a .env file for declare environment variables used for up MySQL service, simple create a .env file in the same directory with docker-compose.yml with this content below:

MYSQL_ROOT_PASSWORD="YOUR-BEST-PASS"
MYSQL_USER="wordpress-user"
MYSQL_PASSWORD="wordpress-pass" 

this file is used for security proposals, for passwords aren't explicity on CLI for example, this file is on .gitignore and .dockerignore files.

### Prerequisites

You need to have the docker installed and running on your machine and git installed only.

### Installing Docker And Docker Compose

For Docker installation check this URL * [Docker Install](https://docs.docker.com/engine/install/ubuntu/)

Since docker is running, clone this repository.

### Cloning this Repo

First check if git protocol is installed, on Debian Based Systems Use:

```
sudo apt install -y git
```

on Red-Hat Based Systems Use:
```
sudo yum install -y git
```

Finally clone this repo with command below (the folder dockerwp-isolate will be created on current directory):
```
git clone https://github.com/renangraciano/dockerwp-isolate.git
```

## Running Docker Compose

Access the directory dockerwp-isolate and run this command below:
```
sudo docker-compose up -d
```
* The proccess will runs in second plan

Expected exit (if success occurs):
```
$ sudo docker-compose up -d
Creating db ... 
Creating db ... done
Creating wordpress ... 
Creating wordpress ... done
Creating webserver ... 
Creating webserver ... done
Creating certbot ... 
Creating certbot ... done
```

Checking Logs:
```
$ sudo docker-compose logs
```

## Built With

* [Docker and Docker Compose](http://www.docker.com/)
* [Wordpresss](https://wordpress.org/)
* [NGINX](https://nginx.org)
* [PHP W-FPM](https://www.php.net/manual/pt_BR/install.fpm.php)
* [CertiBot](https://certbot.eff.org/)

## Authors

* **Renan Souza** - *Initial work* - [GitHub](https://github.com/renangraciano)
