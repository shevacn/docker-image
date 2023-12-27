FROM eclipse-temurin:17-jdk
RUN apt-get update && apt-get install -y tini inetutils-ping dnsutils htop net-tools vim
RUN cp /usr/share/zoneinfo/Asia/Shanghai /etc/localtime && echo 'Asia/Shanghai' >/etc/timezone

RUN curl https://dlcdn.apache.org/maven/maven-3/3.9.4/binaries/apache-maven-3.9.4-bin.tar.gz --output apache-maven-3.9.4-bin.tar.gz
RUN tar -xvf apache-maven-3.9.4-bin.tar.gz && mv apache-maven-3.9.4 /opt/maven
ENV PATH="$PATH:/opt/maven/bin"