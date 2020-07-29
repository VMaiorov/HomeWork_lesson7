FROM ubuntu:18.04
RUN apt update && \
    apt install -y wget && \
    wget https://apache-mirror.rbc.ru/pub/apache/tomcat/tomcat-8/v8.5.57/bin/apache-tomcat-8.5.57.tar.gz -O /tmp/tomcat8.tar.gz && \
    tar -xvf /tmp/tomcat8.tar.gz -C /opt && \
    rm -rf /tmp && \
    rm -rf /opt/apache-tomcat-8.5.57/webapps/examples && \
    rm -rf /opt/apache-tomcat-8.5.57/webapps/docs && \
    rm -rf /opt/apache-tomcat-8.5.57/webapps/ROOT && \
    rm -rf /var/cache/apt
EXPOSE 8080
CMD ["/opt/apache-tomcat-8.5.57/bin/catalina.sh", "run"]    