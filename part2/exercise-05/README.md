# Devops with Docker [exercises](https://devopswithdocker.com/exercises/)

## Part 2

### Exercise 5
- frontend [Docerfile](../../part1/exercise-12/front-end-Dockerfile)
- backend [Docerfile](../../part1/exercise-12/back-end-Dockerfile)
- [docker-compose.yml](docker-compose.yml)


#### Commands run:
- Clone projects to parent directory:
```
git clone https://github.com/docker-hy/backend-example-docker ../backend-example-docker
git clone https://github.com/docker-hy/frontend-example-docker ../frontend-example-docker
```

- Copy docker files:
```
cp ../../part1/exercise-12/front-end-Dockerfile ../frontend-example-docker/Dockerfile
cp ../../part1/exercise-12/back-end-Dockerfile ../backend-example-docker/Dockerfile
```

- create log file:
```
touch logs.txt
```

- build and run images:
```
docker-compose up --build
```
