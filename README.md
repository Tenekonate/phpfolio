# phpfolio

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

Docker Compose
==============

Execute the install composer
----------------------------
To launch the container
```console
docker up -d
```

To go to the php-fpm-8 container
```console
docker-compose exec php-fpm-8 sh
```
To check
```console
composer --version
```

To go to the php-fpm-7 container
```console
docker-compose exec php-fpm-7.4 sh
```
To check
```console
composer --version
```