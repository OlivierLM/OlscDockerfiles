FROM olsc/sshd:jessie
MAINTAINER Olivier LM <olm@unicaen.fr> (@olivierlm)
VOLUME ["/var/www","/etc/apache2"]
# RUN apt-get install --quiet --yes apache2 # security.conf
# RUN apt-get install --quiet --yes libapache2-mod-fcgid # fcgid.conf
# RUN apt-get install --quiet --yes php5-mysql
# RUN apt-get install --quiet --yes php5-cgi
# RUN apt-get install --quiet --yes dokuwiki # interactif :( + dokuwiki.conf
# RUN rm -r /var/lib/dokuwiki/
# RUN ln -s /var/www/aiki-luc/ /var/lib/dokuwiki
ENTRYPOINT ["/sbin/init"]
EXPOSE 22 80 443
