FROM ubuntu

RUN echo "deb http://archive.ubuntu.com/ubuntu precise main universe" > /etc/apt/sources.list
RUN apt-get update
RUN apt-get upgrade

RUN apt-get install -y openssh-server supervisor
ADD sshd.conf /etc/supervisor/conf.d/sshd.conf

RUN mkdir -p /var/run/sshd

RUN echo "root:root" | chpasswd

EXPOSE 22

CMD /usr/bin/supervisord -n
