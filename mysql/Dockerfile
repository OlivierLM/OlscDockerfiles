FROM olsc/sshd:jessie
MAINTAINER Olivier LM <olm@unicaen.fr> (@olivierlm)
VOLUME ["/var/lib/mysql"]
# RUN apt-get install --quiet --yes mysql-server
# RUN sed -i 's/127.0.0.1/0.0.0.0/' /etc/mysql/my.cnf
ENTRYPOINT ["/sbin/init"]
EXPOSE 22 3306
