FROM ubuntu:focal

LABEL author="conanyangqun"
LABEL github="https://github.com/conanyangqun/container-for-bioinformatics"

ARG version="v4.3.0"
ARG base_url="https://github.com/ablab/spades"
ARG DEBIAN_FRONTEND="noninteractive"

# set timezone
RUN apt-get update && apt-get install -y tzdata
RUN ln -sf /usr/share/zoneinfo/Asia/Shanghai /etc/localtime \
    && dpkg-reconfigure --frontend noninteractive tzdata

RUN apt-get update && apt-get install -y \
    curl \
    python3 \
    python3-pip

RUN mkdir /biosoft /biosrc
WORKDIR /biosrc
RUN curl -L "${base_url}/releases/download/${version}/SPAdes-4.3.0-Linux.tar.gz" -o SPAdes-4.3.0-Linux.tar.gz; \
    tar xvf SPAdes-4.3.0-Linux.tar.gz; \
    mv SPAdes-4.3.0-Linux/* /biosoft/;

WORKDIR /
RUN rm -rf /biosrc;apt-get clean

ENV PATH=/biosoft/bin:$PATH
