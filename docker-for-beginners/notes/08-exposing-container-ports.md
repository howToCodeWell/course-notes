To expose a container port use the `-p` argument when running a Docker container. This is done like so
```bash
$ docker run -td --name webserver -p 80:80 ubuntu
```
This will pull Ubuntu if the image doesn't already exist, run a container called webserver and map port 80 from the host machine to the exposed port 80 of the container.

The format of the port argument has two parts split with a `:` symbol.
On the left-hand side of `:` we have the mapped host port.  The right-hand side of `:` is the exposed container port.

For example `-p 80:8080` would map port 80 of the host machine to port 8080 of the container.

The container would be accessed using port 80.

If the argument was `-p 8080:80` then port 80 of the host machine would be mapped to the exposed port 8080 of the container.

The container would be accessed using port 8080.

To see the exposed ports of a container run `docker port <CONTAINER_NAME>`. In this example run `docker port webserver`.
