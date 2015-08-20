# conjur-cluster
To build, make sure you have conjur-appliance image available. Then
```
make images
```

To run, generate an admin password, use it to when running the container

```
password=$(openssl rand -hex 8)
env CONJUR_MASTER_PASSWORD=$password docker-compose up --no-create
```

To stop the containers

```
docker-compose stop
```

Then, to start them again, be sure to provide the --no-create option

```
docker-compose up --no-create
```
