For this exercise I chose to optimize the Java Spring project from exercise 1.13.
The jar is run as a non-root user in a stripped down "openjdk:8-slim" container.

# Image sizes before and after optimization
```
$ docker images | grep javaspring
javaspring-before                              latest              e9c6f43baabe        About a minute ago   590MB
javaspring-after                               latest              ec6f3c5a6514        4 minutes ago        321MB
```
