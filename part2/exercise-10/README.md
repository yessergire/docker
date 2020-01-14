# Devops with Docker [exercises](https://devopswithdocker.com/exercises/)

## Part 2

### Exercise 10
- frontend [Docerfile](front-end-Dockerfile)
- backend [Docerfile](back-end-Dockerfile)
- [docker-compose.yml](docker-compose.yml)

#### Commands run:
- Clone projects to parent directory:
```
git clone https://github.com/docker-hy/backend-example-docker ../backend-example-docker
git clone https://github.com/docker-hy/frontend-example-docker ../frontend-example-docker
```

- Copy docker files:
```
cp ./front-end-Dockerfile ../frontend-example-docker/Dockerfile
cp ./back-end-Dockerfile ../backend-example-docker/Dockerfile
```

- create log file:
```
touch logs.txt
```

- build and run images:
```
docker-compose up --build
```
