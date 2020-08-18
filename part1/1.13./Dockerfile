FROM openjdk:8

RUN git clone https://github.com/docker-hy/spring-example-project.git /mydir

WORKDIR /mydir

RUN ./mvnw package

CMD ["java", "-jar", "./target/docker-example-1.1.3.jar"]