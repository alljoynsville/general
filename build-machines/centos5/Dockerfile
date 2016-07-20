FROM centos:5

RUN yum -y -q install ncurses-devel makedepend vim wget && \
    yum -y -q groupinstall "Development tools" && \
    adduser builder

WORKDIR  /home/builder
USER builder
CMD ["/bin/bash"]
