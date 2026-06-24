FROM ubuntu:focal

LABEL author="conanyangqun"
LABEL github="https://github.com/conanyangqun/container-for-bioinformatics"

ARG version="v4.3.0"
ARG base_url="https://github.com/ablab/spades"
ARG DEBIAN_FRONTEND="noninteractive"

RUN mkdir /biosoft /biosrc
WORKDIR /biosrc
RUN curl -L "${base_url}/releases/download/${version}/SPAdes-4.3.0-Linux.tar.gz" -o SPAdes-4.3.0-Linux.tar.gz; \
    tar xvf SPAdes-4.3.0-Linux.tar.gz; \
    mv SPAdes-4.3.0-Linux/* /biosoft/;

WORKDIR /
RUN rm -rf /biosrc

ENV PATH=/biosoft/bin:$PATH
