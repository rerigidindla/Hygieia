
FROM docker.io/openjdk:8-jre

MAINTAINER Hygieia@capitalone.com

RUN mkdir /hygieia /hygieia/config

COPY *.jar /hygieia/
COPY hpsm-properties-builder.sh /hygieia/

WORKDIR /hygieia

VOLUME ["/hygieia/logs"]

CMD ./hpsm-properties-builder.sh && \
  java -jar hspm-cmdb-collector*.jar --spring.config.location=/hygieia/config/hygieia-hpsm-cmdb-collector.properties

