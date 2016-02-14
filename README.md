# nsolid-docker

This provides the docker images that make it easier to run nsolid in docker. This repository contains the sources for the following docker base images:

- [JustinBeckwith/nsolid-runtime](https://hub.docker.com/r/justinbeckwith/nsolid-runtime/)
- [JustinBeckwith/nsolid-console](https://hub.docker.com/r/justinbeckwith/nsolid-console/)
- [JustinBeckwith/nsolid-hub](https://hub.docker.com/r/justinbeckwith/nsolid-hub/)

Here's [example](/example) of how to tie it all together using Google App Engine.


## Running the console & hub

```
docker run -p 4001:4001 -p 9000:9000 --name nsolid_hub contentful/nsolid-hub
docker run -p 3000:8080 --link nsolid_hub:hub contentful/nsolid-console
```
