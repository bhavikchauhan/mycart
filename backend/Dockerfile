#This is dockerfile for mycart MS frontend layer
FROM centos:7
MAINTAINER mohanraz@gmail.com
RUN yum -y update 
ADD config /opt
RUN yum -y install `cat /opt/packages`
RUN yum -y install `cat /opt/myapp-packages`
ADD code /var/www/html
EXPOSE 80
ENV BACKENDLB=test
ENV MY_DB_HOST=test
ENV MY_DB_NAME_READ=test
ENV MY_DB_NAME_WRITE=test
ENV MY_DB_USER=test
ENV MY_DB_PASS=test

ADD scripts /usr/bin
RUN chmod 755 /usr/bin/startapache
CMD ["startapache"]
#CMD ["apachectl", "-D", "FOREGROWND"]