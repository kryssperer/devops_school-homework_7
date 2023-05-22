FROM ubuntu:20.04

LABEL maintainer="akiyashkin@gmail.com"

#Install needed packages
RUN apt update && apt install wget maven default-jdk -y
RUN apt install git -y

#build boxfuse using maven
WORKDIR /opt/build
RUN git clone https://github.com/boxfuse/boxfuse-sample-java-war-hello.git .
RUN mvn clean package

CMD ["/bin/bash"]