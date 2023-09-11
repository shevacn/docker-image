FROM eclipse-temurin:17-jre
RUN apt-get update && apt-get install -y tini inetutils-ping dnsutils htop net-tools
RUN cp /usr/share/zoneinfo/Asia/Shanghai /etc/localtime && echo 'Asia/Shanghai' >/etc/timezone