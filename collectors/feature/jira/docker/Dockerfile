
FROM docker.io/java:openjdk-8-jdk

MAINTAINER Hygieia@capitalone.com

RUN mkdir  /hygieia

COPY *.jar /hygieia/
COPY jira-properties-builder.sh /hygieia/
RUN chmod +x /hygieia/jira-properties-builder.sh
WORKDIR /hygieia/

VOLUME ["/hygieia/logs"]

CMD ["/bin/bash","/hygieia/jira-properties-builder.sh"]