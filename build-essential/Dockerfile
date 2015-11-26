FROM ubuntu:trusty

MAINTAINER alljoynsville

RUN apt-get update && \
	apt-get update && \
	apt-get -y upgrade && \
	apt-get -y install less wget vim build-essential subversion libncurses5-dev zlib1g-dev gawk gcc-multilib flex git-core gettext libssl-dev && \
	apt-get clean && \
	useradd  --create-home --home-dir /builder --shell /bin/bash builder && \
	rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*

WORKDIR  /builder
USER builder

