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
    curl

# jellyfish.
RUN apt-get update && apt-get install -y \
    jellyfish
