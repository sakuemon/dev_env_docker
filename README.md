# NOTICE
DON'T USE THIS IN PRODUCTION.

# feature
* nginx container
* php-fpm container
* mysql container
* fluentd container
* and configured all container


# customize

## mysql
### USER/PASSWORD/DATABASE
change following line in docker-composer.yml.
```
MYSQL_ROOT_PASSWORD: password
MYSQL_DATABASE: data
MYSQL_USER: s_user
MYSQL_PASSEORD: password
```

### charset
change setting in db/mysql/custom.cnf

### load data
put .sql file into docker-entrypoint-initdb.d folder.

show detail to official repository info. https://hub.docker.com/_/mysql/

## php-fpm
### mount point
change following line inapp/php.yml.
```
- ./php/:/var/www/html
```
