FROM ubuntu:jammy

LABEL author="conanyangqun"
LABEL github="https://github.com/conanyangqun/container-for-bioinformatics"

ARG version="2.6.1"
ARG base_url="https://github.com/fritzsedlazeck/Sniffles"
ARG DEBIAN_FRONTEND="noninteractive"

# set timezone
RUN apt-get update && apt-get install -y tzdata
RUN ln -sf /usr/share/zoneinfo/Asia/Shanghai /etc/localtime \
    && dpkg-reconfigure --frontend noninteractive tzdata

# build packages.
RUN apt-get update && apt-get install -y \
        build-essential \
        cmake \
        curl \
        libncurses5-dev \
        libbz2-dev \
        liblzma-dev \
        zlib1g-dev \
        python3 \
        python3-pip

RUN pip3 --no-cache-dir install sniffles
RUN apt-get clean
WORKDIR /
