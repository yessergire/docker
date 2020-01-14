# Devops with Docker [exercises](https://devopswithdocker.com/exercises/)

## Part 1

### Exercise 15

- [Docerfile](Dockerfile)

#### Commands run:

- Clone project to parent directory:
```
git clone https://github.com/yessergire/SpringApp ../spring-app
```

- build image:
```
docker build --tag spring-app -f Dockerfile ../spring-app
```

- run image:
```
docker run -d -p 8080:8080 spring-app
```
