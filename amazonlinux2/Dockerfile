ARG PLATFORM=amd64
FROM --platform=$PLATFORM amazonlinux:2 as base_amazonlinux2

ENV LANG=en_US.UTF-8

ARG USERNAME=ec2-user

RUN yum update -y && \
    yum install -y sudo coreutils openssh-server which tar make file logrotate cronie && \
    echo '%wheel ALL=(ALL) NOPASSWD:ALL' >> /etc/sudoers && \    
    useradd -m -s /bin/bash -G wheel $USERNAME && \
    chown -R $USERNAME:$USERNAME /var/log

RUN echo "NETWORKING=yes" > /etc/sysconfig/network
CMD [ "/sbin/init" ]
USER $USERNAME
WORKDIR /home/$USERNAME
