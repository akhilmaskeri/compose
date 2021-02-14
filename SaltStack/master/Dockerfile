FROM ubuntu:latest

RUN apt-get update && \
    apt-get -y upgrade

RUN apt-get install -y curl 

RUN curl -L https://bootstrap.saltstack.com -o /tmp/install_salt.sh  && \
    sh /tmp/install_salt.sh -P -M -x python3 && \
    sed -i "s/#auto_accept: False/auto_accept: True/g" /etc/salt/master

ENTRYPOINT [ "salt-master", "-l", "debug", "&"]
