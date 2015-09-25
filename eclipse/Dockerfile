FROM alljoynsville/oracle-jdk8

MAINTAINER alljoynsville

ENV DOWNLOAD_URL http://download.eclipse.org/technology/epp/downloads/release/mars/R/eclipse-cpp-mars-R-linux-gtk-x86_64.tar.gz
ENV INSTALLATION_DIR /usr/local/ 

RUN apt-get update \
 && apt-get install -y curl openssh-server xorg libgtk2.0-0 \
 && mkdir /var/run/sshd \
 && curl "$DOWNLOAD_URL" | tar vxz -C $INSTALLATION_DIR \
 && adduser --disabled-password --quiet --gecos '' eclipse \
 && echo 'eclipse:changemeonfirstlaunch' | chpasswd \
 && chown -R root:eclipse $INSTALLATION_DIR/eclipse \
 && chmod -R 775 $INSTALLATION_DIR/eclipse \
 && apt-get clean \
 && rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*

CMD ["/usr/sbin/sshd", "-D"]
