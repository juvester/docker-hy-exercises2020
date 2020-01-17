FROM openjdk:8 as build-stage
RUN apt-get update && apt-get -y install git && \
    git clone https://github.com/docker-hy/spring-example-project.git /app && \
    cd /app && ./mvnw package

FROM openjdk:8-slim
COPY --from=build-stage /app/target/docker-example-1.1.3.jar /app/docker-example-1.1.3.jar
RUN useradd -m app && \
    chown -R app /app
USER app
WORKDIR /app
EXPOSE 8080
CMD java -jar ./docker-example-1.1.3.jar
