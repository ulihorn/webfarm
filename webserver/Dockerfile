FROM centos:centos6

RUN yum install -y wget

RUN wget http://dl.fedoraproject.org/pub/epel/6/x86_64/epel-release-6-8.noarch.rpm

RUN rpm -Uvh epel-release-6-8.noarch.rpm

RUN yum -y update

RUN yum install -y which sudo httpd php openssh-server unzip

RUN echo -ne "# add the service that we want to start\n/sbin/service httpd start\n/sbin/service sshd start\n" >> ~/.bashrc

RUN wget http://static.oswd.org/designs/3682/bluefreedom3.zip && unzip bluefreedom3.zip && cp -R /bluefreedom3/* /var/www/html/

VOLUME /var/www/html
