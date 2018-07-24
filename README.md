##Detail Guide for intellij 2018.1 and docker

Update : 7/24/2018 2:05 PM

### Intellij Plugin

Search for 'Docker integration' in Plugin

###Windows Docker toolbox (virtual Box)

Ref:https://docs.docker.com/toolbox/faqs/troubleshoot/#solutions

You need Boot2Docker for intellij (Docker toolbox already bundle) 

https://github.com/boot2docker/boot2docker/releases

Download latest

Put it into Docker Cache Folder

`C:\Users\user\.docker\machine\cache`

Then regen the certificate

`docker-machine regenerate-certs default`

restart

`docker-machine restart default`

Set Environment Variable
`eval $(docker-machine env default)`

Check to see it
`docker-machine ls`

##If nothing work

in the
 
 `C:\Users\user\.docker\config.json`
Remove the "credsStore": "wincred" 

## Change Docker connection from TCP/IP to

TCP Socket: 

`https://192.168.99.100:2376`

`C:\Users\user\.docker\machine\machines\default`

##Set up Mongo

https://docs.docker.com/samples/library/mongo/#-via-docker-stack-deploy-or-docker-compose


##Quick Summary

ocker images # 列出目前本地端有抓好哪些 docker image

docker ps # 列出目前正在運行中的 docker container

docker ps -a # 列出目前本地端一共有哪些 docker container (包含已經停止運行的)

docker pull [image_name:version] # 從 docker hub 下載一個特定版本的 docker image

docker pull [image] # 從 docker hub 下載最新版本的 docker image

docker run [image] # 從 docker image 建立一個 docker container 並且運行

docker start [container] # 啟動 docker container

docker stop [container] # 停止 docker container


##Docker network

### Three Thing in Docker
 CMN -Docker
Libnetwork -> Written in Go
 Drivers  -> Bridge, Overlay

   CNM - Docker , Docker
vs CNI - K8s , CoreOS


## swarm (multi-host) vs local (single host)

docker network ls

