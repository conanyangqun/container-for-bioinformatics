FROM continuumio/miniconda3:25.3.1-1

LABEL author="conanyangqun"
LABEL github="https://github.com/conanyangqun/container-for-bioinformatics"

RUN conda create -n pangolin -y && \
    conda install -y \
        -c bioconda \
        -c conda-forge \
        -c defaults \
        -n pangolin \
        pangolin==4.3.1

ENV PATH=/opt/conda/envs/pangolin/bin:$PATH
