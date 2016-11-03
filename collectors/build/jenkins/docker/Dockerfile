
FROM docker.io/java:openjdk-8-jdk

MAINTAINER Hygieia@capitalone.com

RUN mkdir /hygieia

COPY *.jar /hygieia/
COPY jenkins-build-properties-builder.sh /hygieia/
RUN chmod +x /hygieia/jenkins-build-properties-builder.sh
WORKDIR /hygieia

VOLUME ["/hygieia/logs"]

CMD ["/bin/bash", "/hygieia/jenkins-build-properties-builder.sh"]