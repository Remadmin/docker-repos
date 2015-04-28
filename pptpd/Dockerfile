FROM ubuntu:14.04

RUN apt-get update && \
    apt-get install -y pptpd iptables && \
    rm -rf /var/lib/apt/lists/*

RUN echo "username pptpd password *" >> /etc/ppp/chap-secrets && \
    echo "localip 192.168.1.38" >> /etc/pptpd.conf && \
    echo "remoteip 192.168.0.100-200" >> /etc/pptpd.conf && \
    echo "ms-dns 8.8.8.8" >> /etc/ppp/pptpd-options

EXPOSE 1723

ADD run.sh /run.sh

CMD ["/run.sh"]
