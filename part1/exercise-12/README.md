# Devops with Docker [exercises](https://devopswithdocker.com/exercises/)

## Part 1

### Exercise 12

- frontend [Docerfile](front-end-Dockerfile)
- backend [Docerfile](backend-end-Dockerfile)

#### Commands run

- Clone projects to parent directory:
```
git clone https://github.com/docker-hy/backend-example-docker ../backend-example-docker
git clone https://github.com/docker-hy/frontend-example-docker ../frontend-example-docker
```

- build images:
```
docker build --tag frontend -f front-end-Dockerfile ../frontend-example-docker
docker build --tag backend -f back-end-Dockerfile ../backend-example-docker
```

- create log file:
```
touch logs.txt
```

- run images:
```
docker run -dp 5000:5000 frontend
docker run -v  $(pwd)/logs.txt:/src/app/logs.txt -d -p 8000:8000 backend
```
