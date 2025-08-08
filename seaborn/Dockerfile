FROM ubuntu:focal

LABEL author="conanyangqun"
LABEL github="https://github.com/conanyangqun/container-for-bioinformatics"

ARG DEBIAN_FRONTEND="noninteractive"

# set timezone
RUN apt-get update && apt-get install -y tzdata
RUN ln -sf /usr/share/zoneinfo/Asia/Shanghai /etc/localtime \
    && dpkg-reconfigure --frontend noninteractive tzdata

RUN apt-get update && apt-get install -y \
    build-essential \
    cmake \
    curl \
    libncurses5-dev \
    libbz2-dev \
    liblzma-dev \
    zlib1g-dev \
    python3 \
    python3-pip \
    fontconfig \
    fonts-wqy-microhei \
    ttf-wqy-zenhei

RUN pip3 --no-cache-dir install seaborn

RUN apt-get clean
ENV PATH=/biosoft/bin:$PATH
