# Devops with Docker [exercises](https://devopswithdocker.com/exercises/)

## Part 3

### Exercise 6

- [Docerfile](Dockerfile)

#### Commands run:

- Clone project to parent directory:
```
git clone https://github.com/yessergire/SpringApp ../spring-app
```

- build image:
```
docker build --tag optimised-spring-app -f Dockerfile-java ../spring-app
```

- run image:
```
docker run --rm -d -p 8080:8080 optimised-spring-app
```

### Images sizes
- Optimized spring-app size is 143MB
- Before optimization spring-app size is 629MB
