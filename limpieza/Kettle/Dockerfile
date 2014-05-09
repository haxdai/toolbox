FROM debian:jessie

# UPDATE
RUN apt-get -y update

# TOOLS
RUN apt-get install -y -q wget unzip

#JAVA
RUN apt-get install -y openjdk-6-jdk

# INSTALL APP
RUN wget https://copy.com/q8SA6QWSLy1n -O pdi-ce-5.0.1.A-stable.zip
RUN unzip pdi-ce-5.0.1.A-stable.zip 

RUN rm pdi-ce-5.0.1.A-stable.zip

WORKDIR /data-integration

CMD ["./carte.sh", "127.0.0.1", "8081"]

EXPOSE 8081