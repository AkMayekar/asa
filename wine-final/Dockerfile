FROM ubuntu:20.04


ENV DEBIAN_FRONTEND=noninteractive
ENV DISPLAY :0

ENV WINEDEBUG -all

#ENV /root/.wine


RUN apt-get update 
RUN apt-get install wget -y 
RUN dpkg --add-architecture i386 
RUN apt-get update 
RUN apt-get install wine64 -y 

	
	

CMD ["/bin/bash"]


#RUN groupadd -g 999 wine && useradd -u 999 -g wine -G sudo -m -s /bin/bash wine 

#USER wine

	#apt-get install -y gnugp && apt-get install -y gnugp2 && \
	#wget -q0- https://dl.winehq.org/wine-builds/winehq.key | apt-key add - && \
	#mv winehq.key /usr/share/keyrings/winehq-archive.key && \
	#wget -nc https://dl.winehq.org/wine-builds/ubuntu/dists/focal/winehq-focal.sources && \
	#mv winehq-focal.sources /etc/apt/sources.list.d/ && \
	#apt-get update && \
	#apt install --install-recommends winehq-stable -y 
