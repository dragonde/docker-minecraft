FROM phusion/baseimage

ENV DEBIAN_FRONTEND noninteractive

RUN echo "Europe/Madrid" > /etc/timezone
RUN dpkg-reconfigure tzdata

RUN apt-get update
RUN apt-get upgrade -y
RUN apt-get install -y nginx

COPY default /etc/nginx/sites-enabled/default

EXPOSE 8000

CMD service nginx start
