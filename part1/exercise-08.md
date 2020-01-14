# Devops with Docker [exercises](https://devopswithdocker.com/exercises/)

## Part 1

### Exercise 8

- Commands run:

```
touch logs.txt
docker run --rm -d -v $(pwd)/logs.txt:/usr/app/logs.txt devopsdockeruh/first_volume_exercise
```
