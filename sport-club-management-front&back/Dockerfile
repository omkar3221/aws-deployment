# FROM adoptopenjdk/openjdk11:alpine-jre
# COPY target/sportclub.jar sportclub.jar
# ENTRYPOINT ["java","-jar","/sportclub.jar"]
FROM maven:3.6-jdk-12-alpine as build
WORKDIR /wrk
COPY pom.xml .
COPY src src
RUN mvn clean install

FROM adoptopenjdk/openjdk11:alpine-jre
COPY --from=build /wrk/target/sportclub.jar sportclub.jar
ENTRYPOINT ["java","-jar","/sportclub.jar"]
