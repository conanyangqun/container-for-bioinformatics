FROM ubuntu:focal

LABEL author="conanyangqun"
LABEL github="https://github.com/conanyangqun/container-for-bioinformatics"

ARG version="3.0.4"
ARG base_url="https://github.com/yukiteruono/pbsim3"
ARG DEBIAN_FRONTEND="noninteractive"

# set timezone
RUN apt-get update && apt-get install -y tzdata
RUN ln -sf /usr/share/zoneinfo/Asia/Shanghai /etc/localtime \
    && dpkg-reconfigure --frontend noninteractive tzdata

RUN apt-get update && apt-get install -y \
    build-essential \
    cmake \
    curl

# pbsim
RUN mkdir /biosoft /biosrc
WORKDIR /biosrc
RUN curl -L "${base_url}/archive/refs/tags/v${version}.tar.gz" -o "pbsim3.v${vesion}.tar.gz" && \
    tar xvf "pbsim3.v${vesion}.tar.gz" && cd "pbsim3-${version}" && \
    ./configure --prefix=/biosoft && make && make install

RUN apt-get clean
WORKDIR /
RUN rm -rf /biosrc

ENV PATH=/biosoft/bin:$PATH
