FROM alpine
MAINTAINER Slavisa Lukic <lukic@gmx.ch>

RUN apt-get update && \
    apt-get install --no-install-recommends --no-install-suggests -y keepalived && \
    rm -rf /var/lib/apt/lists/*

COPY keepalived /etc/keepalived/
COPY docker-entrypoint.sh /entrypoint.sh

ENTRYPOINT ["/entrypoint.sh"]
