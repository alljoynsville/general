FROM jenkins/jenkins:lts
USER root
RUN apt-get update -yqq && \
    apt-get install -yqq sudo apt-transport-https binutils vim less rsync && \
    curl -fsSL get.docker.com | sudo bash && \
    usermod -aG docker jenkins && \
    curl -LO "https://storage.googleapis.com/kubernetes-release/release/$(curl -s https://storage.googleapis.com/kubernetes-release/release/stable.txt)/bin/linux/amd64/kubectl" && \
    chmod +x ./kubectl && \
    mv ./kubectl /usr/local/bin/kubectl && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
