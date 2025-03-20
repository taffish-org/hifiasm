FROM ghcr.io/taffish-org/debian:12

LABEL maintainer="taffish@163.com"

WORKDIR /root

RUN apt-get update && apt-get install -y curl git gcc g++ make

RUN apt-get update && apt-get install -y zlib1g-dev

RUN curl -LO https://github.com/chhylp123/hifiasm/archive/refs/tags/0.25.0.tar.gz && \
    tar -zxvf /root/0.25.0.tar.gz && cd /root/hifiasm-0.25.0/ && \
    make && cp /root/hifiasm-0.25.0/hifiasm /usr/local/bin/

ENV TAFFISH_ENV=TAFFISH
ENV TAFFISH_NAME=hifiasm
