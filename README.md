# Craft 3 CMS Docker-Compose Configuration



### Requirements
- Images
		[webdevops/php-apache](http://dockerfile.readthedocs.io/en/latest/content/DockerImages/dockerfiles/php-apache.html#webdevops-php-apache)
		[mysql:5.6](https://hub.docker.com/_/mysql/)

### Instructions

* To properly configure Craft CMS to Docker run command:
```shell session
$ composer create-project craftcms/craft web
```

* Create the environment file (.env) and add database settings
```shell session
$ cd web
```
```yaml
  DB_SERVER="mysql"
  DB_USER="root"
  DB_PASSWORD="adminpwd"
  DB_DATABASE="craftdb"
```

* Spin up new Docker containers:
```shell session
$ docker-compose up -d
```
* Install Craft CMS and Done
```curl
 http://localhost:8805/index.php?p=admin
```
