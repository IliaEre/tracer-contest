#
# Build stage
#
FROM maven:3.8.4-openjdk-17 AS build
COPY src /home/app/src
COPY pom.xml /home/app
RUN mvn -f /home/app/pom.xml clean package

# Create image
RUN mvn -f /home/app/pom.xml spring-boot:build-image
