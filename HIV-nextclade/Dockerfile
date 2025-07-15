FROM continuumio/miniconda3:25.3.1-1

LABEL author="conanyangqun"
LABEL github="https://github.com/conanyangqun/HIV-nextclade"

# all softwares.
RUN conda install \
    -y \
    -c conda-forge \
    -c bioconda \
    snakenake \
    biopython \
    numpy \
    pandas \
    treetime
