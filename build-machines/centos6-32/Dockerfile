FROM centos:6.8

RUN yum -y -q install glibc.i686 glibc-devel.i686 libstdc++.i686 libstdc++-devel.i686 zlib.i686 vim && \
    yum -y -q groupinstall "Development tools" && \
    adduser builder

WORKDIR  /home/builder
USER builder
CMD ["/bin/bash"]

