FROM continuumio/miniconda3:25.3.1-1

LABEL author="conanyangqun"
LABEL github="https://github.com/conanyangqun/HIV-nextclade"

# all softwares.
RUN conda install -y -c conda-forge -c bioconda \
    mafft \
    raxml \
    fasttree \
    iqtree \
    vcftools \
    seqkit \
    sqlite \
    nextstrain-augur \
    snakenake \
    biopython \
    numpy \
    pandas \
    treetime \
    nextclade
