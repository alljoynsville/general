FROM ubuntu:trusty

MAINTAINER alljoynsville

RUN apt-get update && \
	apt-get update && apt-get -y upgrade && apt-get -y install less wget vim build-essential scons subversion git-core valgrind cmake && \
	apt-get clean && \
	rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*

WORKDIR  /root/
