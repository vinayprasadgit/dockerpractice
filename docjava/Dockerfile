FROM openjdk:alpine As builder
COPY . /opt/java
WORKDIR /opt/java
COPY Demo.java .
RUN javac Demo.java

FROM alpine 
WORKDIR /app
COPY --from=builder /opt/java /app/

ENTRYPOINT ["Demo","java"]
