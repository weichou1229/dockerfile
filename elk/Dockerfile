FROM openjdk:8-jre

ENV ELASTICSEARCH_VERSION 5.5.1

RUN mkdir -p /elasticsearch

RUN echo "[info] ============= install elasticsearch ${ELASTICSEARCH_VERSION} ============="

RUN wget https://artifacts.elastic.co/downloads/elasticsearch/elasticsearch-${ELASTICSEARCH_VERSION}.tar.gz
RUN sha1sum elasticsearch-${ELASTICSEARCH_VERSION}.tar.gz
RUN tar -xzf elasticsearch-${ELASTICSEARCH_VERSION}.tar.gz

RUN echo "[info] ============= start elasticsearch ${ELASTICSEARCH_VERSION} ============="



EXPOSE 9200

CMD ["elasticsearch-5.5.1/bin/elasticsearch"]