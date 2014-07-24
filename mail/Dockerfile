FROM olsc/sshd:jessie
MAINTAINER Olivier LM <olm@unicaen.fr> (@olivierlm)
RUN apt-get install --quiet --yes postfix
RUN apt-get install --quiet --yes dovecot-imapd
ENTRYPOINT ["/sbin/init"]
EXPOSE 22 25 993
