FROM openjdk:alpine AS Builder
COPY . /opt/java
WORKDIR /opt/java
COPY Sample.java .
RUN javac Sample.java
 
FROM alpine:latest
WORKDIR /root

COPY --from=Builder /opt/java/Sample.class .

#ENTRYPOINT ["java", "Sample"]
CMD java Sample
