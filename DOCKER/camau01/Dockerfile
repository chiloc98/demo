
# Get base image
FROM centos:7

# Author
MAINTAINER "Nguyen Chi Loc"

#Cai dat apache
RUN yum update -y
RUN yum install -y sudo
RUN yum install -y epel-release
RUN yum install -y http://rpms.famillecollet.com/enterprise/remi-release-7.rpm
RUN yum clean all
RUN yum -y install wget
RUN yum -y install httpd
RUN yum -y install --enablerepo=remi,remi-php71 php php-devel php-mbstring php-pdo php-gd php-xml php-mcrypt php-pgsql
 
#Thiet lap thu muc lam viec 
WORKDIR /var/www/html

#copy code tu thu muc code vao image
ADD ./code /var/www/html

# start httpd
CMD ["/usr/sbin/httpd", "-D", "FOREGROUND"]

EXPOSE 80
