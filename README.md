# docker-cheat-sheet
Quick reference guide for Docker commands - not at all exhaustive, just a cheat sheet.


## Building/Running

| task | command |
|:-----|:--------|
|     |       |

## Monitoring/Removing Images

| task | command |
|:-----|:--------|
| list images | `docker images` |
| remove specific image(s) | `docker rmi <image_id> <image_id> ...` |
| remove dangling images | `docker image prune` |
| remove all unused images | `docker image prune --all` |
| remove all images | `docker rmi -f $(docker images -q)` |


## Monitoring/Killing Containers

| task | command | notes|
|:-----|:--------|:-----|
| see running containers | `docker ps` | like `ps` in bash! |
| see most recently launched container | `docker ps -l` | `-l` for last |
| see all containers | `docker ps -a` | `-a` for all |
| see hash of running containers | `docker ps -q` | `-q` for hash |
| see hash of most recent container | `docker ps -ql` | mix `-q` and `-l` for hash of last |
| see hash of all containers | `docker ps -aq` | ditto for `-a` and `-q` |
| see running processes | `docker top id container` | use `id container` |
| kill all running containers | `docker kill $(docker ps -q)` | `kill` only stops running containers |
| kill most recent container | `docker kill $(docker ps -ql)` |
| remove all exited containers | `docker container prune` |
| remove all containers | `docker rm -f $(docker ps -qa)` | `-f` forces `rm` to kill and remove |
| remove old containers | `docker ps -a \| grep 'weeks ago' \| awk '{print $1}' \| xargs docker rm` | removes containers that are created weeks ago |


