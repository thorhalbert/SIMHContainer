FROM ubuntu:latest

ENV DEBIAN_FRONTEND=noninteractive
ENV TZ='America/Los Angeles'
RUN \
	apt-get update -qq && \
	apt-get install -y apt-utils && \
	apt-get dist-upgrade -y && \
	apt-get install -y git build-essential vde2 libsdl-dev libpcap-dev bridge-utils uml-utilities libvdeplug2-dev && \
	apt-get install -y libsdl2-dev libpng-dev libsdl2-ttf-dev  && \
	rm -rf /var/lib/apt/lists/*
RUN \
	mkdir /git && \
	cd /git && \
	git clone https://github.com/simh/simh.git && \
	cd simh && \
	make && \
	cp -vr BIN/* /usr/local/bin/ && \
	cd / && \
	rm -rf /git/simh/
