# Devops with Docker [exercises](https://devopswithdocker.com/exercises/)

## Part 1

### Exercise 5

- Commands run:

```
$ docker run -d --rm -it --name looper-it ubuntu:16.04 sh -c 'echo "Input website:"; read website; echo "Searching.."; sleep 1; curl http://$website;'

$ docker exec -it looper-it bash

root@258ce9f20db7:/# apt update

root@258ce9f20db7:/# apt install -y curl

root@258ce9f20db7:/# exit

$ docker attach looper-it
helsinki.fi
Searching..
<!DOCTYPE HTML PUBLIC "-//IETF//DTD HTML 2.0//EN">
<html><head>
<title>301 Moved Permanently</title>
</head><body>
<h1>Moved Permanently</h1>
<p>The document has moved <a href="http://www.helsinki.fi/">here</a>.</p>
</body></html>
```
