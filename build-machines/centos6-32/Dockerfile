FROM centos:6.8

RUN yum -y install glibc-devel.i686 glibc.i686 libstdc++.i686 libstdc++-devel.i686 zlib.i686 vim && \
    yum -y groupinstall "Development tools"

WORKDIR  /builder
USER builder
CMD ["/bin/bash"]

