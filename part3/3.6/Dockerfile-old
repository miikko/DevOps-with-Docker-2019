FROM openjdk:8

WORKDIR /spring-example
# Project should be pulled and placed in the same directory as this Dockerfile
COPY . .
RUN ./mvnw package

CMD ["java", "-jar", "./target/docker-example-1.1.3.jar"]