FROM anaconda/miniconda:26.3.2

LABEL author="conanyangqun"
LABEL github="https://github.com/conanyangqun/container-for-bioinformatics"


RUN conda tos accept --override-channels --channel https://repo.anaconda.com/pkgs/main;\
    conda tos accept --override-channels --channel https://repo.anaconda.com/pkgs/r;\
    conda install -y -c conda-forge -c bioconda python=3.12 checkm2
