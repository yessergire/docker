# Devops with Docker [exercises](https://devopswithdocker.com/exercises/)

## Part 1

### Exercise 14

- [Docerfile](Dockerfile)

#### Commands

- Clone project to parent directory:
```
git clone https://github.com/docker-hy/rails-example-project ../rails-example-project
```

- build image:
```
docker build --tag clicker-app -f Dockerfile ../rails-example-project
```

- run image:
```
docker run -d -p 3000:3000 clicker-app
```
