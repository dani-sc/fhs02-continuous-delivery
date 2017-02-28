# 01 - Hello World

Build:

```
docker build -t daniel/01-hello-world .
```

Take a look at the created image:

```
docker images
```

Run in background and publish port 3000 to the host system:

```
docker run -d -p 3000:3000 --name hello-world daniel/01-hello-world
```

Stop the container:

```
docker stop hello-world
```

Note: If you would try to start the container again using the same `docker run` command, it would fail, because a container with the name `hello-world` would already exist. You could just omit naming the container: `docker run -d -p 3000:3000 daniel/01-hello-world` and stop the container by using the automatically generated name or, alternatively, the container id in conjunction with the command `docker stop`. Of course, you could also just `docker start hello-world` to bring it up again.

References:

* [Difference between exposing and publishing a port](https://docs.docker.com/docker-cloud/apps/ports/)
* [Dockerfile reference](https://docs.docker.com/engine/reference/builder/)
* [Docker run reference](https://docs.docker.com/engine/reference/run/)
* [docker run](https://docs.docker.com/engine/reference/commandline/run/)
* [docker ps](https://docs.docker.com/engine/reference/commandline/ps/)
* [docker stop](https://docs.docker.com/engine/reference/commandline/stop/)
* [docker start](https://docs.docker.com/engine/reference/commandline/start/)