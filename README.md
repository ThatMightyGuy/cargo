# cargo

## computercraft warehouse suite

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

`get-coords y z x face count` - fetch from these coordinates, from that side (not intended for users because it's harder to use)

`put-coords y z x face` - put items there (not intended for users because it's harder to use)

`get item count` - check db for item, then run `get-coords` on it

`put item` - check db for item, then run `put-coords` on it

`addb item y z x face` - add db entry for item

`help [cargosrv/turtle/cargo]` - show help for $topic, shows all if not specified, probably won't fit on your screen

### cargo remote command overhead

`recon` - reconnect to server

`exit` - poof!


### config files

`@cargosrv/.cargosrv` - main config file for server

`@cargosrv/.warehouse_structure` - item database

`@cargoremote/.cargo` - last connected sid

`@cargoclient/.client` - persistent client data, such as home location etc.


