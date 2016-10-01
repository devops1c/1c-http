
# ubuntu 16.04
FROM phusion/baseimage
MAINTAINER 1cdevops <1cdevops@gmail.com>

RUN apt-get update
RUN apt-get install -y apache2

# Startup Apache
RUN mkdir /etc/service/apache2
ADD apache2.sh /etc/service/apache2/run
RUN chmod +x /etc/service/apache2/run

# Clean up APT when done.
RUN apt-get clean && rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
