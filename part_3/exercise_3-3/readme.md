# Image sizes before optimization
```
$ docker images | grep frontend
frontend            latest              65a42d3129f5        12 minutes ago      465MB

$ docker images | grep backend
backend             latest              fc88bd4a58bb        49 minutes ago      369MB
```
# Image sizes after optimization
```
$ docker images | grep frontend
frontend            latest              04961aba3806        About a minute ago   428MB

$ docker images | grep backend
backend             latest              470483c4b10c        53 seconds ago      332MB
```
