FROM ubuntu:latest

RUN apt-get update 
RUN apt-get -y upgrade
RUN apt-get install -y salt-master
RUN sed -i "s/#auto_accept: False/auto_accept: True/g" /etc/salt/master

ENTRYPOINT [ "salt-master", "-l", "debug", "&"]
