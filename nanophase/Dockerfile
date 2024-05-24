FROM mambaorg/micromamba:1.5.8

LABEL author="conanyangqun"
LABEL github="https://github.com/conanyangqun/container-for-bioinformatics"

RUN micromamba install \
    -y \
    -c nanophase \
    -c defaults \
    -c conda-forge \
    -c bioconda \
    -n base \
    nanophase
