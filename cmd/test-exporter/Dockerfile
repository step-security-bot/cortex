FROM       alpine:3.19@sha256:af4785ccdbcd5cde71bfd5b93eabd34250b98651f19fe218c91de6c8d10e21c5
ARG TARGETARCH
RUN        apk add --no-cache ca-certificates
COPY       test-exporter-$TARGETARCH /test-exporter
ENTRYPOINT ["/test-exporter"]

ARG revision
LABEL org.opencontainers.image.title="test-exporter" \
      org.opencontainers.image.source="https://github.com/cortexproject/cortex/tree/master/cmd/test-exporter" \
      org.opencontainers.image.revision="${revision}"
