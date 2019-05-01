FROM debian:latest
LABEL maintainer="ppichier <ppichier@student.le-101.fr>"
LABEL description="Dockerfile for TeamSpeak serv"

RUN apt-get update -y && \
	apt-get upgrade -y && \
	apt-get install -y wget bzip2 && \
	wget http://dl.4players.de/ts/releases/3.7.1/teamspeak3-server_linux_amd64-3.7.1.tar.bz2 && \
	tar xfvj teamspeak3-server_linux_amd64-3.7.1.tar.bz2

WORKDIR /teamspeak3-server_linux_amd64

RUN touch .ts3server_license_accepted

EXPOSE 9987/udp 10011 30033

ENTRYPOINT ["./ts3server_minimal_runscript.sh" , "createinifile=1"]

#ENTRYPOINT ["ts3server_startscript.sh", "start", "createinifile=1"]
