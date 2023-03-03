FROM maven:3.8.4-jdk-11-slim as builder

WORKDIR /worker

COPY . .

RUN mvn dependency:resolve && mvn package

FROM openjdk:11-jre-slim

WORKDIR /worker/target

COPY --from=builder /worker/target .

CMD java -jar worker-jar-with-dependencies.jar