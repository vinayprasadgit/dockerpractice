FROM alpine
RUN apk add openjdk8
WORKDIR /opt/
ADD https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.55/bin/apache-tomcat-9.0.55.tar.gz .
RUN tar -xvzf apache-tomcat-9.0.55.tar.gz && mv apache-tomcat-9.0.55 tomcat
COPY target/SampleAutoDeploy.war /opt/tomcat/webapps/
EXPOSE 8080
ENTRYPOINT ["/opt/tomcat/bin/catalina.sh", "run"]


