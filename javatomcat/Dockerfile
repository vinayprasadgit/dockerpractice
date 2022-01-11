FROM openjdk:8
WORKDIR /opt/
ADD https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.56/bin/apache-tomcat-9.0.56.tar.gz .
RUN tar -xvzf apache-tomcat-9.0.56.tar.gz && mv apache-tomcat-9.0.56 tomcat
RUN useradd tomcatuser && groupadd tomcatgrp && chown -R tomcatuser:tomcatgrp /opt/tomcat && chmod 777 /opt/tomcat
COPY SampleAutoDeploy.war /opt/tomcat/webapps/
EXPOSE 8080
ENTRYPOINT ["/opt/tomcat/bin/catalina.sh", "run"]
