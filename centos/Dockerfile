FROM centos:6
# Centos7 ssh有问题，换用centos6镜像
MAINTAINER hipeace86 <hipeace86@gmail.com>
RUN yum install epel-release -y && \
    yum update -y && \
    yum install ansible vim openssh-server openssh-clients -y  && \
    chkconfig sshd on && /etc/init.d/sshd start

ADD id_rsa id_rsa.pub /root/.ssh/
RUN cp /root/.ssh/id_rsa.pub /root/.ssh/authorized_keys && \
    /etc/init.d/sshd restart
RUN chmod 600 /root/.ssh/id_rsa && chmod 600 /root/.ssh/authorized_keys && \
    echo '10.1.1.2' >> /etc/ansible/hosts && \
    echo '10.1.1.3' >> /etc/ansible/hosts
