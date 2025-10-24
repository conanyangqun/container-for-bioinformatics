FROM continuumio/miniconda3:25.3.1-1

LABEL author="conanyangqun"
LABEL github="https://github.com/conanyangqun/HIV-nextclade"

ARG DEBIAN_FRONTEND="noninteractive"

# all softwares.
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
        zip

# for snakemake wrappers.
RUN cd /usr/bin && ln -s python3.10 python

# python packages.
RUN pip3 \
    --no-cache-dir \
    install \
    seaborn \
    biopython \
    pysam \
    pandas \
    snakemake \
    phylo-treetime
