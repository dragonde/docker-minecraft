FROM phusion/baseimage

ENV DEBIAN_FRONTEND noninteractive

RUN echo "Europe/Madrid" > /etc/timezone
RUN dpkg-reconfigure tzdata

RUN apt-get update
RUN apt-get upgrade -y
RUN apt-get install -y wget

RUN echo "deb http://overviewer.org/debian ./" >> /etc/apt/sources.list
RUN wget -O - http://overviewer.org/debian/overviewer.gpg.asc | apt-key add -
RUN apt-get update
RUN apt-get install -y minecraft-overviewer 

ENV VERSION 1.8

RUN wget --no-check-certificate https://s3.amazonaws.com/Minecraft.Download/versions/${VERSION}/${VERSION}.jar -P ~/.minecraft/versions/${VERSION}/

ENTRYPOINT ["overviewer.py"]
CMD ["/minecraft/world", "/www"]

