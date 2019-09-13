#This is dockerfile for mycart MS frontend layer
FROM centos:7
MAINTAINER mohanraz@gmail.com
RUN yum -y update
ADD config /opt
RUN yum -y install `cat /opt/apachepackage`
RUN yum -y install `cat /opt/phppackage`
RUN yum -y install `cat /opt/phpprojectmodules` 
ADD code /var/www/html
ENV BACKENDLB=test
EXPOSE 80
ADD scripts /usr/bin
RUN chmod 755 /usr/bin/startapache.sh
CMD ["startapache.sh"]