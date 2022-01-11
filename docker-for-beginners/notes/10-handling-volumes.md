## Types of Docker volumes
There are two type of volumes in Docker.  
The first is a Docker bind mount which is a path from the host machines directory structure to a mount point inside the container.
The second is a Docker named volume. This is a managed mount point in Docker which allows the attachment from multiple containers.

## How to create a bind mount

To create a bind mount use the `-v` argument when running a container. This argument has two parts seperated by a `:`. 

```bash
-v <HOST_DIR>:<CONTAINER_DIR>
```
The left hand-side of the `:`  is the directory structure from the host machine. 
The right hand-side of the `:` is the mount point of the container.  

To mount the host machines home directory into a new directory called data on the container run the following
```bash
$ docker run -it -v ~/home/peterfisher:/data ubuntu bash
```

## How to crate a Docker volume
To create a Docker volume when running a container use the `-v` argument like the bind example but instead of supplying a path from the host machine pass a name of the volume that you wish to create,
```bash
-v <VOLUME_NAME>:<CONTAINER_DIR>
```
To create a Docker volume called `data` which is mounted to the container at the path `/data`  run the following

```bash
$ docker run --name test1 -it -v data:/data ubuntu bash
```
A named Docker volume can also be attached to another container at a different mount point.
The following example attaches the same data Docker volume to a new container called `test2`. The Docker volume is mounted at the path `/data/store` in the container.
```bash
$ docker run --name test2 -it -v data:/data/store ubuntu bash
```
## To list Docker volumes
To list all the docker volumes on the hostmachine run the following
```bash
$ docker volume list
```

## To create a Docker volume
To create a Docker volume without create or running a Docker container run the following
```bash
$ docker volume create <VOLUME_NAME>
```

## How to attach volumes from another container
To mount volumes that are attached from other containers pass the `--volumes-from` argument when creating a new container.
The above command could be simplified by replacing the `-v` argument with the `--volumes-from` argument.  Please note that both the name of the Docker volume and the original mount point inside the container will be copied. 
```bash
$ docker run --name test2 -it --volumes-from test1 ubuntu bash
```

## How to inspect volume configuration
To inspect the mounts of a container run the following command and look for the mounts section in the JSON output.
```bash
$ docker inspect <CONTAINER_NAME_OR_ID>
```


To inspect the configuration of a Docker volume run the following 
```bash
$ docker volume inspect <VOLUME_NAME>
```
This will show the name of the volume, the driver and the mount point of the container.