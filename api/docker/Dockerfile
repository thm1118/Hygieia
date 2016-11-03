
FROM docker.io/java:openjdk-8-jdk

MAINTAINER Hygieia@capitalone.com


ENV SPRING_DATA_MONGODB_DATABASE=dashboarddb
ENV SPRING_DATA_MONGODB_HOST=10.0.1.1
ENV SPRING_DATA_MONGODB_PORT=9999
ENV SPRING_DATA_MONGODB_USERNAME=dashboarduser
ENV SPRING_DATA_MONGODB_PASSWORD=dbpassword


RUN mkdir /hygieia

COPY hygieia /hygieia
COPY properties-builder.sh /hygieia/
#RUN chown root:root /hygieia/properties-builder.sh
RUN chmod +x /hygieia/properties-builder.sh

WORKDIR /hygieia

VOLUME ["/hygieia/logs"]

EXPOSE 8080

CMD ["/bin/bash", "/hygieia/properties-builder.sh"]