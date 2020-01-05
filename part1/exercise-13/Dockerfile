FROM openjdk:8u232-jdk

WORKDIR /src/app

COPY . ./

RUN ./mvnw package

EXPOSE 8080

CMD ["/usr/local/openjdk-8/bin/java", "-jar", "./target/docker-example-1.1.3.jar"]
