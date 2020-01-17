# Image sizes before optimization
```
$ docker images | grep 'frontend\|backend'
backend                                        latest              85bcd5088e6d        20 minutes ago      333MB
frontend                                       latest              cb5a2c46c6e0        21 minutes ago      429MB
```
# Image sizes after optimization
```
$ docker images | grep 'frontend\|backend'
backend                                        latest              b9025990ae7c        About a minute ago   139MB
frontend                                       latest              ceee26a882da        2 minutes ago        236MB
```
