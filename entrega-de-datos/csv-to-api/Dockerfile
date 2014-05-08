FROM debian:jessie

# UPDATE
RUN apt-get -y update
RUN apt-get -y update

#SHIMS
RUN dpkg-divert --local --rename --add /sbin/initctl
RUN ln -s /bin/true /sbin/initctl
ENV DEBIAN_FRONTEND noninteractive

# EDITORS
RUN apt-get install -y -q vim nano

# TOOLS
RUN apt-get install -y -q curl wget git


# PHP
RUN apt-get install -y -q php5 php5-cli php5-dev php-pear php5-fpm php5-common php5-mcrypt php5-gd php-apc

# APACHE
RUN apt-get install -y -q apache2 libapache2-mod-php5

# INSTALL APP
RUN a2enmod php5 rewrite
RUN rm -rf /var/www/*
RUN git clone https://github.com/project-open-data/csv-to-api.git /var/www
ADD application /var/www/csv-to-api

# RESET

ENV DEBIAN_FRONTEND dialog

## CONFIG
ENV RUNNABLE_USER_DIR /var/www/csv-to-api
ENV RUNNABLE_SERVICE_CMDS /etc/init.d/apache2 restart
