## Docker Machine environments

Each Docker Machine will have its own set of environment variables.  These can be access using the following command
```bash
docker-machine env <name>
```

Where `<name>` is the name of the selected Machine.
The output would be similar to the following

```bash
 export DOCKER_TLS_VERIFY="1"
 export DOCKER_HOST="tcp://172.16.62.130:2376"
 export DOCKER_CERT_PATH="/Users/<yourusername>/.docker/machine/machines/default"
 export DOCKER_MACHINE_NAME="default"
```

## Connect to a Docker Machine
To switch to a Docker Machine the environment variables must be exported to your shell. This is done like so
```bash
eval "$(docker-machine env default)"
```
Once the Docker Machine environment variables have been evaluated to the current shell the containers within that machine will be accessible by your local Docker commands.
