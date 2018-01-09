# load-util

## Purpose
`load-util` is a small, sharp script for the sole purpose of easily (i.e. lazily) loading an ssh private key identity from a USB thumbdrive into the SSH authentication agent on a Mac. 

## Usage
### By a number of hours
```bash
/Volumes/my_thumbdrive/load-util -t 5
# or
/Volumes/my_thumbdrive/load-util --hours 5
```
Will call the proper `ssh-add` command to load your key into the agent for 5 hours.

### Till end of day
```bash
/Volumes/my_thumbdrive/load-util --eod
```
Will do some arithmetic and load your key into the agent until 5 p.m. local time



## Caveats
* this was only tested on a Mac and assumed to only work on Macs
* your private key must be named `id_rsa` 
* your private key must be co-located with this load-util script
