#From centos:version
FROM java:7
MAINTAINER wuyang wuyang@aiisen.com

ENV RESIN_VERSION=resin-pro-3.1.13

WORKDIR /app/

ADD resin-pro-3.1.13.tar.gz /app/

RUN mv /app/resin-pro-3.1.13/ /app/resin && \
mkdir -p /app/www/

COPY resin.conf /app/resin/conf
COPY index.html /app/www/

#CMD ["/bin/bash"]

EXPOSE 8080
ENTRYPOINT ["/app/resin/bin/httpd.sh"]

#https://hub.docker.com/r/misswuyang
#docker build -t resin:3 .
#docker run --name web8080 -d -p 8080:8080 resin:3
#docker run --name web8080 -d -p 8080:8080 -v /Users/wuyang/Documents/work/docker/centos6-resin3/html:/app/www resin:3
#docker run --name web8080 -d -p 8080:8080 -v /www/conf/resin.conf:/app/resin/conf/resin.conf -v /www/proj:/app/www resin:3
#docker run --name web8080 -d -p 8080:8080 -v /www/dushu:/app/www misswuyang/centos6-resin:java7
