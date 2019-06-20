ARG BUILD_FROM
FROM $BUILD_FROM

MAINTAINER David Ramos <info@davidramosweb.com>

ENV LANG C.UTF-8

# Install requirements for add-on
RUN apk add --update bash jq curl && rm -rf /var/cache/apk/*
    
COPY cloudflare.sh /
RUN chmod a+x /cloudflare.sh

CMD [ "/cloudflare.sh" ]
