FROM debian:jessie

# UPDATE
RUN apt-get -y update
RUN apt-get -y upgrade

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
RUN git clone https://github.com/philipashlock/DataBeam.git /var/www

# RESET

ENV DEBIAN_FRONTEND dialog

## CONFIG
ENV RUNNABLE_USER_DIR /var/www/DataBeam
ENV RUNNABLE_SERVICE_CMDS /etc/init.d/apache2 restart
