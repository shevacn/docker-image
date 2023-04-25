FROM eclipse-temurin:17-jre
RUN apt-get update && apt-get install tini
RUN cp /usr/share/zoneinfo/Asia/Shanghai /etc/localtime && echo 'Asia/Shanghai' >/etc/timezone