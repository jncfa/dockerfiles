FROM ghcr.io/typst/typst:latest as typst-vendor

FROM ghcr.io/jncfa/ubuntu-dev:latest as base

COPY --from=typst-vendor /bin/typst /usr/local/bin/typst
