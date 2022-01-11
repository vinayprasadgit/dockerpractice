FROM openjdk:8
COPY . /opt/java
WORKDIR /opt/java
COPY Demo.java .
VOLUME /opt/java_volA:/opt/java
RUN javac Demo.java
CMD ["java","Demo"]

