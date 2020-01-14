# Devops with Docker [exercises](https://devopswithdocker.com/exercises/)

## Part 1

### Exercise 13

- [Docerfile](Dockerfile)

#### Commands

- Clone project to parent directory:
```
git clone https://github.com/docker-hy/spring-example-project ../spring-example-project
```

- build image:
```
docker build --tag spring-button -f Dockerfile ../spring-example-project
```

- run image:
```
docker run -d -p 8080:8080 spring-button
```
