FROM continuumio/miniconda3:25.3.1-1

LABEL author="conanyangqun"
LABEL github="https://github.com/conanyangqun/container-for-bioinformatics"

# conflicts.
#RUN conda install -y \
#    -c conda-forge \
#    -c bioconda \
#    augur

RUN conda install -y \
    -c conda-forge \
    -c bioconda \
    mafft \
    raxml \
    fasttree \
    iqtree \
    vcftools \
    seqkit \
    sqlite

# augur
RUN pip3 install --no-cache-dir nextstrain-augur
