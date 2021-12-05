Provide the user option(`--user`) to the Docker run command to run a container as a certain user.

```bash
$ docker run <CONTAINER_NAME> run --user <USER_ID>:<USER_GROUP>
```

- `<CONTAINER_NAME>` is the name of the container
- `<USER_ID>` is the UID of the user
- `<USER_GROUP>` is the GID of the user

Please note that the user and group must be available in the container.