# Dockerfile for OpenRA dedicated server

## Example
```sh
docker run -e 'NAME=Docker_Server_1' \
           -e 'MOTD=Muß man wissen!' \
           -e 'ADVERTISE_ONLINE=True' \
           -p 1234:1234 \
           -d johannesw/openra

docker run -e 'NAME=Docker_Server_2' \
           -e 'MOTD=Muß man wissen!' \
           -e 'EXTERNAL_PORT=4444' \
           -e 'ADVERTISE_ONLINE=True' \
           -p 4444:1234 \
           -d johannesw/openra
```

## Settings

| ENV  | EXAMPLE VALUE   | DESCRIPTION  | DEFAULT  |   |
|---|---|---|---|---|
| NAME  | Silo and Wall Rush  |  Server name  |   |   |
| MOTD  | Have fun | MOTD, on server join   |   |   |
| LOCK_BOTS  | True  |  Disable bots  |  False |   |
| EXTERNAL_PORT  | 1234  |  External port, used for server list registration  |  1234 |   |
| ADVERTISE_ONLINE  | True  | Register with public  server list |  False |   |
| MOD  | ra  |  OpenRA Mod "Red Alert"  | ra |   |
| MAP  | a967ccc7fc250d89d6945d63ca9ee5e0f539eeb7 | Load initial map with id, see [Resource Center][1]  |  |   |
| PASSWORD  | whatever | Password to connect |  |   |


Various options can be set by using environment variables, see:
https://github.com/rmoriz/openra-dockerfile/blob/master/bin/start.sh

[1]: http://resource.openra.net/maps/110

## FYI

Seems like an example server with RA-mod needs at least 500MB of memory, maybe even more.

## Copyright & License

Copyright © 2014 [Roland Moriz](https://roland.io), see LICENSE.txt
