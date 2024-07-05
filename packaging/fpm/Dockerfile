FROM alpine:3.19@sha256:af4785ccdbcd5cde71bfd5b93eabd34250b98651f19fe218c91de6c8d10e21c5

RUN apk add --no-cache \
        ruby \
        ruby-dev \
        ruby-etc \
        gcc \
        git \
        libc-dev \
        libffi-dev \
        make \
        rpm \
        tar \
        && gem install --no-document fpm

COPY package.sh /
ENTRYPOINT ["/package.sh"]

ARG revision
LABEL org.opencontainers.image.title="fpm" \
        # TODO: should this label point to the fpm source code?
        org.opencontainers.image.source="https://github.com/cortexproject/cortex/tree/master/packaging/fpm" \
        org.opencontainers.image.revision="${revision}"
