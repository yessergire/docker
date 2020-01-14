# Devops with Docker [exercises](https://devopswithdocker.com/exercises/)

## Part 1

### Exercise 4

- The secret message is 'Docker is easy'
- Commands run:
```
$ docker run -d --name looper devopsdockeruh/exec_bash_exercise
$ docker exec -it looper bash
root@b30d1db6cfc4:/usr/app# tail -f logs.txt
Wed, 01 Jan 2020 17:22:18 GMT
Wed, 01 Jan 2020 17:22:21 GMT
Wed, 01 Jan 2020 17:22:24 GMT
Wed, 01 Jan 2020 17:22:27 GMT
Secret message is:
"Docker is easy"
```
