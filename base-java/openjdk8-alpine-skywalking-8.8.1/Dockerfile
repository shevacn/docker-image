FROM openjdk:8-jdk-alpine
RUN sed -i 's/dl-cdn.alpinelinux.org/mirrors.ustc.edu.cn/g' /etc/apk/repositories
RUN apk add -U tzdata
ENV TZ=Asia/Shanghai
RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone

#安装curl、arthas
RUN apk add curl && curl -O https://arthas.aliyun.com/arthas-boot.jar

RUN apk add --no-cache tini
COPY sw-8.8.1/ /data/plugins/sw/