FROM ubuntu:18.04
RUN apt update && \
    apt install -y default-jdk maven git && \
    git clone https://github.com/boxfuse/boxfuse-sample-java-war-hello.git && \
    mvn package -f /boxfuse-sample-java-war-hello/pom.xml