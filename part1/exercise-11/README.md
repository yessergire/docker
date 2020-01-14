# Devops with Docker [exercises](https://devopswithdocker.com/exercises/)

## Part 1

### Exercise 11

- [Docerfile](Dockerfile)

#### Commands run

- Clone project to parent directory:
```
git clone https://github.com/docker-hy/backend-example-docker ../backend-example-docker
```

- build image:
```
docker build --tag backend -f Dockerfile ../backend-example-docker
```

- create log file:
```
touch logs.txt
```

- run image:
```
docker run -v  $(pwd)/logs.txt:/src/app/logs.txt -d -p 8000:8000 backend
```
