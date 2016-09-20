FROM ubuntu:trusty

RUN apt-get update && \
    apt-get -yqq install gawk wget git-core diffstat unzip texinfo gcc-multilib \
      build-essential chrpath socat libsdl1.2-dev xterm \
      subversion wget unzip python vim && \
    apt-get clean && \
    useradd -m builder && \
    echo 'builder ALL=NOPASSWD: ALL' > /etc/sudoers.d/openwrt
RUN sudo -iu builder git clone git://git.yoctoproject.org/poky
USER builder
WORKDIR /home/builder
