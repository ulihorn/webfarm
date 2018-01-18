FROM centos:centos6

RUN yum install -y wget

RUN wget http://dl.fedoraproject.org/pub/epel/6/x86_64/epel-release-6-8.noarch.rpm

RUN rpm -Uvh epel-release-6-8.noarch.rpm

RUN yum -y update

RUN yum install -y which sudo httpd php openssh-server

RUN echo -ne "# add the service that we want to start\n/sbin/service httpd start\n/sbin/service sshd start\n" >> ~/.bashrc