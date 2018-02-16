FROM alpine:3.5

MAINTAINER galushko86@gmail.com



RUN apk --update upgrade && \
    apk add --update bind && \
    rm -rf /var/cache/apk/*


ADD run.sh /run.sh
RUN chmod 750 /run.sh


VOLUME ["/etc/bind", "/var/log/named"]

EXPOSE 53 53/udp

WORKDIR /etc/bind/


CMD ["/run.sh"]
