ARG version=7.17.1
FROM docker.elastic.co/elasticsearch/elasticsearch:${version}
LABEL maintainer Yuki Takei <yuki@weseek.co.jp>

RUN bin/elasticsearch-plugin install analysis-kuromoji
RUN bin/elasticsearch-plugin install analysis-icu

RUN { \
        echo 'http.host: 0.0.0.0'; \
        echo 'http.cors.enabled: true'; \
        echo 'http.cors.allow-origin: "*"'; \
    } > /usr/share/elasticsearch/config/elasticsearch.yml

