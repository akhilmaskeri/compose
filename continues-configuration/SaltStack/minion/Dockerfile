FROM ubuntu:latest

RUN apt-get update && apt-get -y upgrade
RUN apt-get install -y salt-minion
RUN apt-get install -y vim

RUN sed -i "s/#master: .*/master: salt-master_1/g" /etc/salt/minion

ENTRYPOINT [ "salt-minion", "-l","debug" ]
