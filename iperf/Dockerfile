FROM centos
MAINTAINER Xin
LABEL description="for iperf test"
RUN yum -y update
RUN yum -y install openssh-server
RUN echo 'root:123456' | chpasswd
RUN ssh-keygen -t rsa -f /etc/ssh/ssh_host_rsa_key -N ""
RUN ssh-keygen -t ecdsa -f /etc/ssh/ssh_host_ecdsa_key -N ""
RUN ssh-keygen -t ed25519 -f /etc/ssh/ssh_host_ed25519_key -N ""
#RUN sed -i 's/UsePAM yes/UsePAM no/' /etc/ssh/sshd_config
RUN yum -y install iperf3
RUN echo "/usr/sbin/sshd" >> ~/.bashrc
