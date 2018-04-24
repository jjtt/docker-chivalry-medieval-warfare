# Chivalry: "Medieval Warfare" docker for the native linux server

## Cookbook 

* create docker volume on host (/opt/chivalry in example below)
* add liberal r/w at least for uid=1000, gid=999 (user "steam" inside container)
* docker build -t chivalry_server .
* docker run -ti -v /opt/chivalry:/opt/chivalry -p 0.0.0.0:8000:8000/udp -p 0.0.0.0:27015:27015/udp --name chivalry chivalry_server

## Features / tested with
* works with mod LSMOD, Blackknight, giantslayers
* most maps (hoth excluded)
* game.ini can be changed reliable
* mods / workshop items can be changed reliable

## known issues
* scripts can be optimized
* no restart if the server has a coredump
