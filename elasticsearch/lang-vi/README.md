https://github.com/duydo/elasticsearch-analysis-vietnamese

```shell
docker build -t shevacn/elasticsearch-lang-vi-7.17.1 --build-arg ES_VERSION=7.17.1 .

docker push shevacn/elasticsearch-lang-vi-7.17.1

docker run -d --restart always\
           -p 9200:9200 \
           -p 9300:9300 \
           -e "discovery.type=single-node" \
           -e "ELASTIC_PASSWORD=YOUR-PASSWORD" \
           -e "xpack.security.enabled=true" \
           -e "ES_JAVA_OPTS=-Xms512m -Xmx512m" \
           -v /data/esdata:/usr/share/elasticsearch/data \
           shevacn/elasticsearch-lang-vi-7.17.1
```