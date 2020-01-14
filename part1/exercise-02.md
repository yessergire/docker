
# Devops with Docker [exercises](https://devopswithdocker.com/exercises/)

## Part 1

### Exercise 2

- List containers:

```
$ docker ps -a
CONTAINER ID        IMAGE               COMMAND             CREATED             STATUS              PORTS               NAMES
fce43346f6ba        nginx               "nginx -g 'daemon of…"   7 seconds ago       Up 4 seconds        80/tcp              nginx-3
29a2707f3467        nginx               "nginx -g 'daemon of…"   11 seconds ago      Up 9 seconds        80/tcp              nginx-2
1510ea868c86        nginx               "nginx -g 'daemon of…"   16 seconds ago      Up 13 seconds       80/tcp              nginx-1
```

- Stop containers:

```
$ docker stop fce 29a 151
fce
29a
151
```

- Remove containers:
```
$ docker container prune
WARNING! This will remove all stopped containers.
Are you sure you want to continue? [y/N] y
Deleted Containers:
fce43346f6badf13928f18530f4faa14d89a8176bccf029bdeb19e275ca5574b
29a2707f3467ad006e0848def19796600eb44f73cc7983f6a0ea369ceff079dc
1510ea868c8674bad7803c08cfd2fc3b73f6c760365f6697026a3ebfd73084cb

Total reclaimed space: 0B
```

- List containers:
```
$ docker ps -a
CONTAINER ID        IMAGE               COMMAND             CREATED             STATUS              PORTS               NAMES
```

- List images:
```
$ docker images
REPOSITORY                             TAG                 IMAGE ID            CREATED             SIZE
nginx                                  latest              c7460dfcab50        4 days ago          126MB
hello-world                            latest              fce289e99eb9        12 months ago       1.84kB
```

- Remove images:
```
$ docker rmi c746 fce2
Untagged: nginx:latest
Untagged: nginx@sha256:8aa7f6a9585d908a63e5e418dc5d14ae7467d2e36e1ab4f0d8f9d059a3d071ce
Deleted: sha256:c7460dfcab502275e9c842588df406444069c00a48d9a995619c243079a4c2f7
Deleted: sha256:3e51598e49c550f8b212a07c6ff2ed47a09eeb637f67d1b3c5468e9a8ee646e3
Deleted: sha256:a8b9a5643b3cc8082997d3d2fbaf4b53213ff80aa4169226be8b3768ae6e3605
Untagged: hello-world:latest
Untagged: hello-world@sha256:4fe721ccc2e8dc7362278a29dc660d833570ec2682f4e4194f4ee23e415e1064
Deleted: sha256:fce289e99eb9bca977dae136fbe2a82b6b7d4c372474c9235adc1741675f587e
Deleted: sha256:af0b15c8625bb1938f1d7b17081031f649fd14e6b233688eea3c5483994a66a3
```

- List images:
```
$ docker images
REPOSITORY                             TAG                 IMAGE ID            CREATED             SIZE
```
