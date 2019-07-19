ARG BUILD_FROM
FROM $BUILD_FROM

MAINTAINER David Ramos <info@davidramosweb.com>


ENV LANG C.UTF-8

# Install requirements for add-on
RUN apk update && apk add bash jq iw hostapd && rm -rf /var/cache/apk/*

COPY hostapd.conf /
COPY interfaces /etc/network/interfaces
COPY run.sh /
RUN chmod a+x /run.sh

CMD [ "/run.sh" ]
