# Devops with Docker [exercises](https://devopswithdocker.com/exercises/)

## Part 1

### Exercise 10

- [Docerfile](Dockerfile)

#### Commands run

- Clone project to parent directory:
```
git clone https://github.com/docker-hy/frontend-example-docker ../frontend-example-docker
```

- build image:
```
docker build --tag frontend -f Dockerfile ../frontend-example-docker
```

- run image:
```
docker run -d -p 5000:5000 frontend
```
