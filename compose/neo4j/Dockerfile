FROM ubuntu:14.10
MAINTAINER Etienne Peiniau <etienne.peiniau@gmail.com>

# required tools
RUN chmod 777 /tmp
RUN apt-get update
RUN apt-get install -y wget 

# install neo4j
RUN wget -O - http://debian.neo4j.org/neotechnology.gpg.key | apt-key add -
RUN echo 'deb http://debian.neo4j.org/repo stable/' > /etc/apt/sources.list.d/neo4j.list
RUN apt-get update 
RUN apt-get install -y neo4j-enterprise=2.1.7

# add custom libs and conf
COPY conf/* /etc/neo4j/

# expose REST and SHELL ports
EXPOSE 7474 
EXPOSE 1337

# run neo4j
CMD ["/var/lib/neo4j/bin/neo4j", "console"]
