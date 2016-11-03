
FROM docker.io/java:openjdk-8-jdk

MAINTAINER Hygieia@capitalone.com

RUN mkdir /hygieia

COPY *.jar /hygieia/
COPY bitbucket-properties-builder.sh /hygieia/
RUN chmod +x /hygieia/bitbucket-properties-builder.sh
WORKDIR /hygieia

VOLUME ["/hygieia/logs"]

CMD ["/bin/bash","/hygieia/bitbucket-properties-builder.sh"]