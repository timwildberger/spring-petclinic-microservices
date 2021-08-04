# we will use openjdk 8 with alpine as it is a very small linux distro
FROM openjdk:8-jre-alpine3.9

RUN wget -O dockerize.tar.gz https://github.com/jwilder/dockerize/releases/download/v0.6.1/dockerize-alpine-linux-amd64-v0.6.1.tar.gz
RUN tar xzf dockerize.tar.gz
RUN chmod +x dockerize

# copy the packaged jar file into our docker image
COPY target/spring-petclinic-discovery-server-2.5.1.jar /spring-petclinic-discovery-server.jar

EXPOSE 8761
EXPOSE 9095

# set the startup command to execute the jar
CMD ["java", "-jar", "/spring-petclinic-discovery-server.jar"]
