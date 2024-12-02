FROM ubuntu:focal

LABEL author="conanyangqun"
LABEL github="https://github.com/conanyangqun/container-for-bioinformatics"

ARG version="1.21"
ARG base_url="https://github.com/samtools/"

RUN apt-get update && apt-get install -y \
    build-essential \
    cmake \
    curl \
    libncurses5-dev \
    libbz2-dev \
    liblzma-dev \
    zlib1g-dev

RUN mkdir /biosoft /biosrc
WORKDIR /biosrc
RUN for tag in htslib samtools bcftools; \
    do program="${tag}-${version}"; \
    curl -L "${base_url}/${tag}/releases/download/${version}/${program}.tar.bz2" -o "${program}.tar.bz2"; \
    tar xvf "{program}.tar.bz2" && cd "${program}"; \
    ./configure --prefix=/biosoft && make && make install; \
    cd ../; done

RUN apt-get clean
WORKDIR /
RUN rm -rf /biosrc

ENV PATH=/biosoft/bin:$PATH
