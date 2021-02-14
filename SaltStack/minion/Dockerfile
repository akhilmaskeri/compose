FROM ubuntu:latest

RUN apt-get update && \
    apt-get -y upgrade

RUN apt-get install -y curl

RUN curl -L https://bootstrap.saltstack.com -o /tmp/install_salt.sh  && \
    sh /tmp/install_salt.sh -P -x python3 && \
    sed -i "s/#master: .*/master: salt-master/g" /etc/salt/minion

ENTRYPOINT [ "salt-minion", "-l","debug" ]
