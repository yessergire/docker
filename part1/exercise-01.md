# Devops with Docker [exercises](https://devopswithdocker.com/exercises/)

## Part 1

### Exercise 1

Commands run:
```
docker run -d --name nginx-1 nginx 
docker run -d --name nginx-1 nginx 
docker run -d --name nginx-1 nginx 
docker ps
```

Output:
```
CONTAINER ID        IMAGE               COMMAND                  CREATED             STATUS              PORTS               NAMES
fce43346f6ba        nginx               "nginx -g 'daemon of…"   7 seconds ago       Up 4 seconds        80/tcp              nginx-3
29a2707f3467        nginx               "nginx -g 'daemon of…"   11 seconds ago      Up 9 seconds        80/tcp              nginx-2
1510ea868c86        nginx               "nginx -g 'daemon of…"   16 seconds ago      Up 13 seconds       80/tcp              nginx-1
```
