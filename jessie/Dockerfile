FROM debian:jessie
RUN echo "deb http://repos.um.ac.ir/debian jessie main contrib non-free" > /etc/apt/sources.list \
&&  echo "deb http://repos.um.ac.ir/debian-security jessie/updates main" >> /etc/apt/sources.list
RUN apt-get -y update \
&&  apt-get -y install vim net-tools tcpdump psmisc dnsutils binutils telnet rsyslog cron curl python python-mysqldb
COPY crontab /etc/
RUN /etc/crontab
CMD service rsyslog start && service cron start && tail -f /var/log/syslog
