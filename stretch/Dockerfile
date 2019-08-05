FROM debian:stretch
RUN echo "#!/bin/bash" > /etc/rc.local \
&&  echo "exit 0" >> /etc/rc.local \
&&  chmod +x /etc/rc.local \
&&  echo "deb http://repos.um.ac.ir/debian stretch main contrib non-free" > /etc/apt/sources.list \
&&  echo "deb http://repos.um.ac.ir/debian-security stretch/updates main" >> /etc/apt/sources.list
RUN apt-get -y update \
&&  apt-get -y install vim net-tools tcpdump psmisc dnsutils binutils telnet rsyslog cron curl python
