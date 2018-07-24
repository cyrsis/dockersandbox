##Detail Guide for intellij 2018.1 and docker

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

## Change Docker connection from TCP/IP to

TCP Socket: 

`https://192.168.99.100:2376`

`C:\Users\user\.docker\machine\machines\default`
