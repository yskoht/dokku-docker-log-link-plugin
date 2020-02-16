
# dokku-docker-log-link-plugin

A plugin to create symbolic link to docker container log file after deploy.

## For what?

I want to track the docker container log file, but it is hard.
Because in dokku, the contaienr log path changes each time the app is deployed.
This plugin creates symbolic link at fixed path (`/var/log/dokku/containers`) with fixed prefix (`your app name`) after each deploy.

## Install

```bash
$ dokku plugin:install https://github.com/yskoht/dokku-docker-log-link-plugin
```

## Usage

```
$ git push dokku master
...
...
...
-----> Creating symbolic link
       src: /var/lib/docker/containers/a9932592017070d0a940f4134f4a5d83360e429c5dbe7808df3c011b3b46e24f/a9932592017070d0a940f4134f4a5d83360e429c5dbe7808df3c011b3b46e24f-json.log
       dst: /var/log/dokku/containers/app-a9932592017070d0a940f4134f4a5d83360e429c5dbe7808df3c011b3b46e24f.log
```

## License

This software is released under the MIT License, see LICENSE.

