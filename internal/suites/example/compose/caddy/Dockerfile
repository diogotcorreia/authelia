FROM caddy:2.9.1-builder@sha256:3c1a90ada80f1b9239c2248a3b3f846501849fc8d934e288442ae4456c82a1e1 AS builder

RUN xcaddy build fix-empty-copy-headers

FROM caddy:2.9.1@sha256:116bea95dd70e611b4b46f5fc0fc931aa1b2acc75c0e8903c88a93a713d57e6d

COPY --from=builder /usr/bin/caddy /usr/bin/caddy
