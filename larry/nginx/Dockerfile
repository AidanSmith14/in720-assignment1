FROM ubuntu:16.04
MAINTAINER Aidan Smith
ENV REFRESHED_AT 2016-08-30

RUN apt-get -qqy update && apt-get -qqy install nginx

ADD nginx_proxy_server.conf /etc/nginx/nginx.conf

EXPOSE 80

CMD ["nginx", "-g", "daemon off;"]
