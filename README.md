# parityDaemon

### Description:
parity ethereum client's daemon that monitors the PID and auto restarts it if it dies

## Prerequisite

sudo apt-get install `screen`

## Configuration

1) Create a bash script to spin up parity the way you want to spin it up( arguements, configs etc.)
2) Replace line 23 `~/parity` to the path of your parity run script folder. (example: `/path/to/script/location`
3) Replace line 24 `./run` with `./[your script name]`

## Managing

#### Starting : 
``screen -dmS "paritydaemon" ./paritydaemon`` where `./paritydaemon` is the path to this file
#### Stopping : 
`screen -r "paritydaemon"` then press `ctrl + a` then `ctrl + d`
#### Monitoring: 
`screen -r "paritydaemon"` will show logs with time stamps of any incidents occured
