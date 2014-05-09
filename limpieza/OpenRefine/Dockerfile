FROM debian:jessie

# UPDATE
RUN apt-get -y update

# TOOLS
RUN apt-get install -y -q curl wget git

#JAVA
RUN apt-get install -y openjdk-7-jre

# INSTALL APP
RUN wget https://github.com/OpenRefine/OpenRefine/releases/download/2.5/google-refine-2.5-r2407.tar.gz
RUN tar zxvf google-refine-2.5-r2407.tar.gz

RUN rm google-refine-2.5-r2407.tar.gz

WORKDIR /google-refine-2.5

CMD ["./refine"]

EXPOSE 3333