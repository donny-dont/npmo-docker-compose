FROM alpine:3.4

RUN apk update && \
    apk upgrade && \
    apk add ca-certificates curl && \
    rm -rf /var/cache/apk/*

ENV CONFD_VERSION=0.12.0-alpha3

RUN curl -L -o /bin/confd \
    "https://github.com/kelseyhightower/confd/releases/download/v$CONFD_VERSION/confd-$CONFD_VERSION-linux-amd64" && \
    chmod +x /bin/confd

ENTRYPOINT ["/bin/confd"]
CMD ["-onetime", "-backend", "env"]
