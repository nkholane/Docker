FROM debian

ENV TS3SERVER_LICENSE=accept

WORKDIR	/home/teamspeak

RUN apt-get update
RUN apt-get upgrade
RUN apt-get install -y wget
RUN apt-get install -y bzip2
RUN wget http://dl.4players.de/ts/releases/3.12.1/teamspeak3-server_linux_amd64-3.12.1.tar.bz2
RUN tar -xvf teamspeak3-server_linux_amd64-3.12.1.tar.bz2

EXPOSE 9987/udp
EXPOSE 30033
EXPOSE 1001

WORKDIR teamspeak3-server_linux_amd64

ENTRYPOINT sh ts3server_minimal_runscript.sh

#docker build -t ex01 .
# docker run --rm -p 9987:9987/udp -p 10011:10011 -p 30033:30033 ex01 
