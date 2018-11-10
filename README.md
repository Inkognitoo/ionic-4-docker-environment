Based on [beevelop](https://github.com/beevelop/docker-ionic) images. Big thanks him for it.

Tested only for Linux. If you want it for MAC or WIN feel free to make pull request.

# START NEW PROJECT #

fork this repo to you  
clone it locally

copy **.env.example** to **.env** and replace any environment value you want

run `docker-compose up -d` for start docker container  
run `docker-compose exec ionic bash` for going into container

run `cd /tmp && ionic start $PROJECT_NAME blank --no-git && cp -rn /tmp/$PROJECT_NAME ~/ && cd ~/$PROJECT_NAME` for creating new ionic project

run `ionic serve` and open [localhost:8100](http://localhost:8100) for check is it work correctly

If you want act like a root, going into container via command  
`docker-compose exec --user=root ionic bash`

## Problem solving ##
### Can't run debug on android device ###
If command `ionic cordova run android` can't find device try:
1. Active _debug by usb_ on android device
2. Kill adb server on host machine `adb kill-server`
