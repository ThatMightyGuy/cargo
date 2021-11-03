# cc-cargos

### computercraft warehouse suite

## features

1. multiturtling (untested, not enough ender pearls to make modems lol)
2. processing any number of simultaneous user requests, but there's no way to queue requests yet
3. dynamic turtle reconnecting
4. remote access support
5. adding item database entries on the fly
6. ??? (WIP)

## how to use

### commands

`clients` - client list

`uclients` - update client list (reconnect to turtles)

`getcoords y z x face count` - fetch from these coordinates, from that side (not intended for users because it's harder to use)

`putcoords y z x face` - put items there (not intended for users because it's harder to use)

`get item count` - check db for item, then run `get-coords` on it

`put item` - check db for item, then run `put-coords` on it

`addb item y z x face` - add db entry for item

`listb` - show valid item names

`help [cargosrv/turtle/cargo]` - show help for $topic, shows all if not specified, probably won't fit on your screen

`movehome sid y z x` - moves turtle home position

`resetcoords sid y z x face` - sets turtle current coordinates and direction, in case something breaks

### cargo remote command overhead

`recon` - reconnect to server

`newcon` - reset .cargo and exit, thus allowing you to connect to a different server

`exit` - poof!


### config files

`@cargosrv/.cargosrv` - main config file for server

`@cargosrv/.cargostructure` - item database

`@cargoremote/.cargo` - last connected sid

`@cargoclient/.cargoclient` - persistent client data, such as home location etc.

## first-time setup

`@cargoserver$ edit .cargosrv` and update modem location (statefile not yet implemented)

included `@cargoserver/.cargostructure` is my current warehouse setup. it won't fit you, so i advise you to remove all entries and add them yourself, either manually or by using the `addb` command ~~or cope~~
