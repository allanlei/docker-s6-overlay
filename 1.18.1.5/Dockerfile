FROM        alpine:3.4

ENV         VERSION=1.18.1.5
RUN         apk --no-cache add --virtual .build-deps \
                curl && \
            curl -L https://github.com/just-containers/s6-overlay/releases/download/v$VERSION/s6-overlay-amd64.tar.gz | tar xvz && \
            apk del .build-deps
ENTRYPOINT  ["/init"]
