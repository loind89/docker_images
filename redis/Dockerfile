# Use an official Centos runtime as a base image
FROM centos
# Upgrading system
#RUN yum -y upgrade
RUN yum -y install epel-release

#fix 404 error 
RUN sed -i -e 's/mirrorlist/#mirrorlist/g' /etc/yum.repos.d/epel.repo
RUN sed -i -e 's/#baseurl/baseurl/g' /etc/yum.repos.d/epel.repo

RUN yum -y update


RUN yum -y install redis
EXPOSE      6379
ENTRYPOINT  ["/usr/bin/redis-server"]