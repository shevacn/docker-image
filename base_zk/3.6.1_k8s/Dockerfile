FROM zookeeper:3.6.1

RUN ln -s /apache-zookeeper-3.6.1-bin /opt/zookeeper 
ENV ZOOCFGDIR=/opt/zookeeper/conf

COPY start-zookeeper /opt/zookeeper/bin
COPY zookeeper-ready /opt/zookeeper/bin
COPY sources.list /etc/apt/sources.list

RUN chmod +x /opt/zookeeper/bin/start-zookeeper /opt/zookeeper/bin/zookeeper-ready && \
    chown zookeeper:zookeeper /opt/zookeeper/bin/start-zookeeper /opt/zookeeper/bin/zookeeper-ready && \
    apt-get update &&  apt-get -y install vim net-tools procps telnet inetutils-ping

WORKDIR /opt