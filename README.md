# To prevent any confusion please read this file carefully.

We value your effort and time, due to that we built this project base to save your time.

We want you to spend your time on creating infrastructure and application not general things like creating docker-compose etc.

Considering that please do not modify project base. We put everything you need inside this project. Instead of that we expect you to code.

## Installation

Before you start you need to install docker. Then run;
```shell
docker compose up -d
```

### Important
Do not forget to add flag `-d` because this image is php-cli image. To make container alive forever it runs `tail -f /dev/null`.

## To connect the container

```shell
docker container exec -it jagaad_php_cli /bin/sh
```

## Working directory

`/var/www/html` is main project folder. **Do not change it.**

## Debugging
Xdebug is installed in this image. Feel free to use it via your IDE.

```
PHP 8.2.9 (cli) (built: Aug 17 2023 23:22:07) (NTS)
Copyright (c) The PHP Group
Zend Engine v4.2.9, Copyright (c) Zend Technologies
    with Xdebug v3.2.2, Copyright (c) 2002-2023, by Derick Rethans
```

XDebug environment variables are already configured on `docker-compose.yml:7`

## Composer
If you need composer, you can find it inside `bin` folder.

## Preinstalled packages

See `composer.json` for preinstalled packages that you may want to use it.

## Project requirements and test case

See [PROJECT.md](project.md)