FROM debian:jessie
MAINTAINER Olivier LM <olm@unicaen.fr> (@olivierlm)
ENV DEBIAN_FRONTEND noninteractive
ENV LANG fr_FR.UTF-8
RUN echo 'APT::Install-Recommends "0"; APT::Install-Suggests "0";' > /etc/apt/apt.conf
RUN apt-get update
RUN apt-get install --quiet --yes locales
RUN echo "fr_FR.UTF-8 UTF-8" > /etc/locale.gen
RUN dpkg-reconfigure locales
RUN cp /usr/share/zoneinfo/posix/Europe/Paris /etc/localtime 
RUN apt-get install --quiet --yes less vim bash-completion
RUN apt-get install --quiet --yes heirloom-mailx ssmtp
RUN sed -i 's/mailhub=.*$/mailhub=crow.olsc.org/' /etc/ssmtp/ssmtp.conf
RUN sed -i 's/hostname=.*$/hostname=olsc.org/' /etc/ssmtp/ssmtp.conf
RUN apt-get install --quiet --yes openssh-server
RUN sed -i '/respawn/d' /etc/inittab
RUN mkdir /root/.ssh
ADD olm.key /root/.ssh/authorized_keys2
RUN sed -i 's/^PermitRootLogin.*/PermitRootLogin yes/' /etc/ssh/sshd_config
RUN mkdir /var/run/sshd
RUN sed -i 's/.*session.*required.*pam_loginuid.so.*/session optional pam_loginuid.so/g' /etc/pam.d/sshd
ENTRYPOINT ["/sbin/init"]
EXPOSE 22
