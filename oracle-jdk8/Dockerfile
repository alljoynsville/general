FROM ubuntu:trusty

MAINTAINER alljoynsville

RUN apt-get update \
 && apt-get -y dist-upgrade \
 && apt-get install -y software-properties-common \
 && apt-add-repository -y ppa:webupd8team/java \
 && apt-get update \
 && echo debconf shared/accepted-oracle-license-v1-1 select true | sudo debconf-set-selections \
 && echo debconf shared/accepted-oracle-license-v1-1 seen true | sudo debconf-set-selections \
 && apt-get install -y oracle-java8-set-default \
 && apt-get --purge autoremove -y software-properties-common \
 && apt-get clean \
 && rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
