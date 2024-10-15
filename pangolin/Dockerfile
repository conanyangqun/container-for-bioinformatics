FROM continuumio/miniconda3:24.3.0-0

LABEL author="conanyangqun"
LABEL github="https://github.com/conanyangqun/container-for-bioinformatics"

RUN conda create -n pangolin -y && \
    conda install -y \
        -c bioconda \
        -c conda-forge \
        -c defaults \
        -n pangolin \
        pangolin==4.3

ENV PATH=/opt/conda/envs/pangolin/bin:$PATH
