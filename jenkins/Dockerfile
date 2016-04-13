FROM jenkins
USER root
RUN apt-get update && \
    apt-get -y install docker.io && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
    

