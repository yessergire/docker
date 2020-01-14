# Devops with Docker [exercises](https://devopswithdocker.com/exercises/)

## Part 1

### Exercise 16

#### [Container location](http://app-heroku-example.herokuapp.com)

#### Commands run:
```
docker pull devopsdockeruh/heroku-example
docker tag devopsdockeruh/heroku-example registry.heroku.com/app-heroku-example/web
heroku container:login
docker push registry.heroku.com/app-heroku-example/web
heroku container:release web --app=app-heroku-example
heroku open --app=app-heroku-example
```
