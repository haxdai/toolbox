FROM debian:jessie

# UPDATE
RUN apt-get -y update

# EDITORS
RUN apt-get install -y -q vim nano

# TOOLS
RUN apt-get install -y -q curl wget git


# PYTHON
RUN apt-get install -y -q python2.7 python-setuptools
RUN easy_install pip


# INSTALL APP
RUN pip install petl

