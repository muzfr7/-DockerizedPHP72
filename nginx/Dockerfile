FROM nginx:latest

MAINTAINER "Muzafar Jatoi <muzfr7@gmail.com>"

RUN apt-get update \
	&& apt-get install -y nano

# Set TimeZone
RUN rm /etc/localtime
RUN ln -s /usr/share/zoneinfo/Asia/Karachi /etc/localtime
RUN "date"

COPY default.conf /etc/nginx/conf.d/