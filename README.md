# parityDaemon


### Description:
parity ethereum client's daemon that monitors the PID and auto restarts it if it dies

## Prerequisite

sudo apt-get install `screen`

### Installing
`git clone https://github.com/dipenjoshi/parityDaemon.git`

`sudo cp ./parityDaemon/parityDaemon /usr/local/bin`

`sudo chmod +x /usr/local/bin/parityDaemon`

`sudo cp ./parityDaemon/parityd.service /lib/systemd/system`

## Configuration
**(edit file /usr/local/bin/parityDaemon)** by typing `sudo nano /usr/local/bin/parityDaemon`
1) Create a bash script to spin up parity the way you want to spin it up( arguements, configs etc.)
2) Replace line 23 `~/parity` to the path of your parity run script folder. (example: `/path/to/script/location/[your script name]`
3) Replace line 24 `./run` with `./[your script name]`

## Managing

#### Starting : 
`sudo systemctl start parityd`
#### Stopping: 
`sudo systemctl stop parityd`
#### Status:
`sudo systemctl status parityd`
