FROM centos
MAINTAINER Xin
LABEL description="for iperf test"
RUN yum -y update \
    && yum -y install openssh-server \
    && yum -y install iperf3
RUN ssh-keygen -t rsa -f /etc/ssh/ssh_host_rsa_key -N "" \
    && ssh-keygen -t ecdsa -f /etc/ssh/ssh_host_ecdsa_key -N "" \
    && ssh-keygen -t ed25519 -f /etc/ssh/ssh_host_ed25519_key -N ""
RUN echo "root:123456" | chpasswd \
    && echo "/usr/sbin/sshd" >> ~/.bashrc
#RUN sed -i 's/UsePAM yes/UsePAM no/' /etc/ssh/sshd_config
