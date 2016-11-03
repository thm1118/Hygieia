
FROM docker.io/java:openjdk-8-jdk

MAINTAINER Hygieia@capitalone.com

RUN \
  mkdir /hygieia

COPY *.jar /hygieia/
COPY jenkins-cucumber-test-properties-builder.sh /hygieia/
RUN chmod +x /hygieia/jenkins-cucumber-test-properties-builder.sh
WORKDIR /hygieia

VOLUME ["/hygieia/logs"]

CMD ["/bin/bash","/hygieia/jenkins-cucumber-test-properties-builder.sh"]

