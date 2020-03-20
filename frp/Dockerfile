FROM alpine
MAINTAINER 15093565100@163.com
ADD frp.tar /tmp/
RUN mkdir /etc/frp/ && mv /tmp/frps.ini /etc/frp/ && mv /tmp/frps /usr/bin/ && rm -rf /tmp/*
EXPOSE 7000 80 443
VOLUME /etc/frp/
ENTRYPOINT /usr/bin/frps -c /etc/frp/frps.ini 
    
