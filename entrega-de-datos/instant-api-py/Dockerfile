FROM debian:jessie

# UPDATE
RUN apt-get -y update

# EDITORS
RUN apt-get install -y -q vim nano

# TOOLS
RUN apt-get install -y -q curl wget git


# PYTHON
RUN apt-get install -y -q python2.7 

# INSTALL APP
RUN git clone https://github.com/jbradforddillon/instant-api-py.git
RUN cd instant-api-py
# RUN python2.7 instant-api-py/instant-api-py --port 5000 --file instant-api-py/source.json

ENV DEBIAN_FRONTEND dialog

EXPOSE 5000

