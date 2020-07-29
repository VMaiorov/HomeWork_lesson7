FROM alpine:latest
ENV TOMCAT_VERSION 8.5.50
RUN apk update && apk upgrade && \
    apk add openjdk8 && \
    apk add ca-certificates wget                                                                                                                      $
EXPOSE 8080
RUN wget --quiet --no-cookies https://archive.apache.org/dist/tomcat/tomcat-8/v${TOMCAT_VERSION}/bin/apache-tomcat-${TOMCAT_VERSION}.tar.gz -O /tmp/tomcat.tgz && \
tar xzvf /tmp/tomcat.tgz -C /opt && \
mv /opt/apache-tomcat-${TOMCAT_VERSION} /opt/tomcat && \
rm /tmp/tomcat.tgz && \
rm -rf /opt/tomcat/webapps/examples && \
rm -rf /opt/tomcat/webapps/docs && \
rm -rf /opt/tomcat/webapps/ROOT
CMD ["/opt/tomcat/bin/catalina.sh", "run"]
