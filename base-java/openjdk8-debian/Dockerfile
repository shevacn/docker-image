FROM openjdk:8-jdk
RUN apt-get update && apt-get install tini
RUN cp /usr/share/zoneinfo/Asia/Shanghai /etc/localtime && echo 'Asia/Shanghai' >/etc/timezone