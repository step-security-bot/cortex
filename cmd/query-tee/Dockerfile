FROM       alpine:3.19@sha256:af4785ccdbcd5cde71bfd5b93eabd34250b98651f19fe218c91de6c8d10e21c5
ARG TARGETARCH

RUN        apk add --no-cache ca-certificates
COPY       query-tee-$TARGETARCH /query-tee
ENTRYPOINT ["/query-tee"]

ARG revision
LABEL org.opencontainers.image.title="query-tee" \
      org.opencontainers.image.source="https://github.com/cortexproject/cortex/tree/master/tools/query-tee" \
      org.opencontainers.image.revision="${revision}"
