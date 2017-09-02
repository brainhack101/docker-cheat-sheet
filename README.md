# docker-cheat-sheet
Quick reference guide for Docker commands - not at all exhaustive, just a cheat sheet.


## Building/Running

| task | command |
|:-----|:--------|
|     |       |

## Monitoring/Removing Images

| task | command |
|:-----|:--------|
|     |       |

## Monitoring/Killing Containers

| task | command | notes|
|:-----|:--------|:-----|
| see running containers | `docker ps` | like `ps` in bash! |
| see most recently launched container | `docker ps -l` | `-l` for last |
| see all containers | `docker ps -a` | `-a` for all |
| see hash of running containers | `docker ps -q` | `-q` for hash |
| see hash of most recent container | `docker ps -ql` | mix `-q` and `-l` for hash of last |
| see hash of all containers | `docker ps -aq` | ditto for `-a` and `-q` |
| kill all running containers | `docker kill $(docker ps -q)` | `kill` only stops running containers |
| kill most recent container | `docker kill $(docker ps -ql)` |
| remove all exited containers | `docker rm $(docker ps -qa)` | `rm` only removes exited containers |
| remove all containers | `docker rm -f $(docker ps -qa)` | `-f` forces `rm` to kill and remove |
