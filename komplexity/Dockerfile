FROM continuumio/miniconda3:24.3.0-0

LABEL author="conanyangqun"
LABEL github="https://github.com/conanyangqun/container-for-bioinformatics"

RUN conda create -n komplexity -y && \
    conda install -y \
        -c eclarke \
        -n komplexity \
        komplexity

ENV PATH=/opt/conda/envs/komplexity/bin:$PATH
