FROM phusion/baseimage

ENV DEBIAN_FRONTEND noninteractive

RUN echo "Europe/Madrid" > /etc/timezone
RUN dpkg-reconfigure tzdata

RUN apt-get update
RUN apt-get upgrade -y

RUN apt-get install -y python-software-properties
RUN add-apt-repository ppa:webupd8team/java -y

RUN apt-get update
RUN echo oracle-java7-installer shared/accepted-oracle-license-v1-1 select true | /usr/bin/debconf-set-selections

RUN apt-get install -y oracle-java7-installer
RUN apt-get install -y wget

RUN mkdir /minecraft
RUN wget -O /minecraft/minecraft_server.jar https://s3.amazonaws.com/Minecraft.Download/versions/1.8/minecraft_server.1.8.jar
RUN chmod +x /minecraft/minecraft_server.jar

VOLUME /minecraft
WORKDIR /minecraft

COPY eula.txt /minecraft/
COPY server.properties /minecraft/
COPY ops.txt /minecraft/

EXPOSE 25565

CMD java -Xmx1024M -Xms1024M -jar minecraft_server.jar nogui
