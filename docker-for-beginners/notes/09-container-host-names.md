To change the hostname of a container use the `-h` or the `--hostname` argument when running a container. 

For example to create a container with the hostname of `abc` run the following

```bash
docker run -it -h abc ubuntu bash
```
This will create a Ubuntu container with the hostname `abc`. This container will be running bash and the terminal will have a similar output
```bash
$ root@abc:/#
```

Setting a hostname of a container will also alter the containers host file. 

To check this run the following `cat /etc/host`

```bash
127.0.0.1 localhost

// Other entries

172.17.0.2 abc abc
```

Please note, your container IP will be different.