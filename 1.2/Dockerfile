FROM alpine
MAINTAINER Slavisa Lukic <lukic@gmx.ch>

RUN apk --no-cache --no-progress upgrade && \
    apk --no-cache --no-progress add keepalived && \
    rm -rf /tmp/*

COPY keepalived /etc/keepalived/
COPY docker-entrypoint.sh /entrypoint.sh

ENTRYPOINT ["/entrypoint.sh"]
