FROM ubuntu:xenial

MAINTAINER alljoynsville

ENV DOWNLOAD_URL http://download.eclipse.org/technology/epp/downloads/release/neon/3/eclipse-cpp-neon-3-linux-gtk-x86_64.tar.gz
ENV INSTALLATION_DIR /usr/local

RUN apt-get -yqq update \
 && apt-get -yqq install vim curl wget openssh-server xorg libgtk2.0-0 libssl-dev build-essential scons sudo \
    subversion git-core valgrind cmake default-jre \
 && mkdir /var/run/sshd \
 && curl "$DOWNLOAD_URL" | tar xz -C $INSTALLATION_DIR/ \
 && useradd -m eclipse \
 && echo 'eclipse ALL=NOPASSWD: ALL' > /etc/sudoers.d/eclipse \
 && chown -R root:eclipse $INSTALLATION_DIR/eclipse \
 && chmod -R 775 $INSTALLATION_DIR/eclipse \
 && ln -s $INSTALLATION_DIR/eclipse/eclipse /usr/bin/ \
 && apt-get clean \
 && rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*

CMD ["/usr/sbin/sshd", "-D"]
