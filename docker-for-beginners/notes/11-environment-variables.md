## How to set environment variables

To set environment variables when running a Docker container use the `-e` argument. The argument has two parts separated by an `=` symbol.
The left-hand side is the variable name and the right-hand side is the variable value.

```bash
$ docker run -it -e MODE=test ubunutu bash
```

In the above example an Ubuntu Docker container would be created with the environment variable called `MODE` set with the value of `test`.

Multiple environment variables can be set by adding extra `-e` arguments to the Docker run command.

```bash
$ docker run -it -e MODE=test -e DOC_ROOT=/var/www ubunutu bash
```

## How to use an environment variable file

A file containing environment variables can be supplied to the Docker run command.  Each variable needs to go on a single line in this file

```bash
// .env.list
MODE=test
DOC_ROOT=/var/www
```

To supply this file of environment variables to the Docker run command use the `--env-file` argument.
```bash
$ docker run -it --env-file=./env.list ubunutu bash
```

## How to override environment variables

Variables that are supplied with the `-e` argument will override variables supplied by the `env-file`

In the following example the `MODE` environment variable will be set to `dev`

```bash
// .env.list
MODE=test
DOC_ROOT=/var/www
```

```bash
$ docker run -it --env-file=./env.list -e MODE=dev ubunutu bash
```