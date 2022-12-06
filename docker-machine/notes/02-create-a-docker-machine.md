## Creating a Machine
Run the following to create a Docker Machine

Where the <driver> flag defines the virtual environment driver used to create the machine. <name> is the name that is given to the Machine. By default the name `default` will be used.
```bash
docker-machine create --driver=<driver> <name>
```

## Listing Machines
To list the Docker Machines use the `ls` command like so
```bash
docker-machine ls 

NAME      ACTIVE   DRIVER       STATE     URL                         SWARM   DOCKER   ERRORS
default   *        virtualbox   Running   tcp://192.168.99.187:2376           v1.9.1
```