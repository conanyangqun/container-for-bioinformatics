FROM continuumio/miniconda3:25.1.1-2

LABEL author="conanyangqun"
LABEL github="https://github.com/conanyangqun/container-for-bioinformatics"

# below is failed command.
# conda install -y -c bioconda graphaligner==1.0.20, need jemalloc
# conda install -y -c bioconda -c conda-forge graphaligner==1.0.20, failed, protobuf 3.14.0 needs python 3.9
# conda install -y -c conda-forge -c bioconda python==3.9.0 graphaligner==1.0.20
# conda install -y -c conda-forge -c bioconda python==3.9 graphaligner==1.0.20
# conda install -y -c conda-forge -c bioconda python==3.10 graphaligner==1.0.20
# conda install -y -c bioconda -c conda-forge graphaligner will install graphaligner-1.0.13, latest is v1.0.20
