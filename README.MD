# Thernity Fivem server

![GitHub](https://img.shields.io/github/license/Thernity/image-fivem)
![Docker Pulls](https://img.shields.io/docker/pulls/thernity/fivem)

This docker image allows you to run a server for FiveM, a modded GTA multiplayer.
The container should be stopped so fivem can be configured to the user requirements in the server.cfg.

## Licence Key

A freely obtained licence key is required to use this server, which should be declared as `$LICENCE_KEY`. A tutorial on how to obtain a licence key can be found [here](https://forum.fivem.net/t/explained-how-to-make-add-a-server-key/56120)



## Quickstart

```yml
fivem:
  image: thernity/fivem

  stdin_open: true
  tty: true

  volumes:
    # You must provide a server config file
    - ./server.cfg:/srv/server.cfg

    - ./resources:/srv/resources
    - ./cache:/srv/cache

  ports:
    - "30120:30120/tcp"
    - "30120:30120/udp"
```

