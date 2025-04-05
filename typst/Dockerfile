FROM ghcr.io/typst/typst:latest as typst-vendor

FROM ubuntu:latest as base

RUN apt-get update && apt-get install -y \
    curl python3 python3-pip \
    && apt-get clean \
    && rm -rf /var/lib/apt/lists/*

COPY --from=typst-vendor /bin/typst /usr/local/bin/typst
