
FROM docker.io/java:openjdk-8-jdk

MAINTAINER Hygieia@capitalone.com

RUN \
  mkdir /hygieia

COPY *.jar /hygieia/
COPY github-properties-builder.sh /hygieia/
RUN chmod +x /hygieia/github-properties-builder.sh
WORKDIR /hygieia

VOLUME ["/hygieia/logs"]

CMD ["/bin/bash", "/hygieia//github-properties-builder.sh"]


