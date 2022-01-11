## How to alter a container
To alter the Docker image first create and run container from the image.

```bash
$ docker run -it <IMAGE_ID> <COMAND_YOU_WANT_TO_RUN>
```

Running a bash shell in the container would be similar to the following:
```bash
$ docker run -it xyz123 /bin/bash
```

Once inside the containers bash shell you can alter the container.  An example would be to be install applications or run a package upgrade.
In the below example the packages will be updated and npm will be installed.
```bash
root@abc123:/# apt-get update
root@abc123:/# apt-get install npm
root@abc123:/# exit
```

A container is a snapshot of an image and each container has a unique ID.

The container is now different to the underlying Docker image. Subsequent containers of the original Docker image would not contain npm or the package updates as these are only stored against this container.
To save these changes to the Docker image the container alterations need to be committed. This will create a new Docker image with its own tag and ID. This Docker image can be pushed to a Docker repository for future use.

## How to save the changes
The ID of the altered container is needed to commit the changes.

Run `docker ps -a` to get the ID of the altered container.

Create a new Docker image tag by running  `docker commit <CONTAINER_ID> <IMAGE_TAG>` 

The `CONTAINER_ID` is the ID of the updated container. The `IMAGE_TAG` is a human-readable tag name for the Docker image. 
For example this could be 
```bash
$ docker commit abc123 ubuntu-npm
```

This creates a new `IMAGE_ID` which can be used to create a new Docker container. Any containers made from this new Docker image will have the updated packages and npm installed.

To test this run `docker run -it <NEW_IMAGE_ID> npm -v`