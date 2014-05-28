FROM olsc/sshd:jessie
MAINTAINER Olivier LM <olm@unicaen.fr> (@olivierlm)
RUN apt-get install --quiet --yes bind9
ADD named.conf.local /etc/bind/
ADD db.olsc.org /var/cache/bind/
ENTRYPOINT ["/sbin/init"]
EXPOSE 22 53
