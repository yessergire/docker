FROM ubuntu:16.04

WORKDIR /src/app

COPY . ./

RUN apt update && apt install curl -y
RUN curl -sL https://deb.nodesource.com/setup_10.x | bash

RUN apt install -y nodejs
RUN npm install

EXPOSE 5000

CMD ["/usr/bin/npm","start"]
