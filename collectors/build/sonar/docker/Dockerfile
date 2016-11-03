
FROM docker.io/java:openjdk-8-jdk

MAINTAINER Hygieia@capitalone.com

RUN \
  mkdir /hygieia

COPY *.jar /hygieia/
COPY sonar-codequality-properties-builder.sh /hygieia/
RUN chmod +x /hygieia/sonar-codequality-properties-builder.sh
WORKDIR /hygieia

VOLUME ["/hygieia/logs"]

CMD ["/bin/bash","/hygieia/sonar-codequality-properties-builder.sh"]

