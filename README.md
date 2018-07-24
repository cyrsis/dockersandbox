##Detail Guide for intellij and docker

###Windows Docker toolbox (virtual Box)

You need Boot2Docker for intellij (Docker toolbox already bundle) 

https://github.com/boot2docker/boot2docker/releases

Download latest

Put it into Docker Cache Folder

`C:\Users\user\.docker\machine\cache`

Then regen the certificate

`docker-machine regenerate-certs default`

restart

`docker-machine restart default`

Check
`eval $(docker-machine env default)`


