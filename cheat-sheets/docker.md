# Docker Cheat Sheet

## Docker Login (Docker Cloud and Docker Hub) 

### Set Username
```sh
$ export DOCKER_ID_USER="username"
```

### Log in 
```sh
$ docker login
```

## Tag a Docker Image   
```sh
$ docker tag my_image $DOCKER_ID_USER/my_image
```

## Push Docker Image
```sh
$ docker push $DOCKER_ID_USER/my_image
```

