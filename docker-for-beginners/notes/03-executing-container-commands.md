To run a command in a running container use the `exec` command like so
```bash
$ docker exec -it <CONTAINER_NAME> <COMMAND> <COMMAND_ARUGMENTS>
```

- `<CONTAINER_NAME>` could be the container ID or the container name.
- `<COMMAND>` is the command that you want to run in the container.
- `<COMMAND_ARGUMENTS>` are the arguments to pass to the command.

The options `-it` are optional.  This will  keep the STDIN open and allocate pseudo-TTY
For other options please check the Docker documentation.

## Examples

Run codeception in a docker container

```bash
$ docker exec -it app bin/codept run unit
```

Access the Python interpreter

```bash
$ docker exec -it app pythonß
```
