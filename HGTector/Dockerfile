FROM continuumio/miniconda3:25.1.1-2

LABEL author="conanyangqun"
LABEL github="https://github.com/conanyangqun/container-for-bioinformatics"

# stuck, maybe network?
# RUN conda install -y -c conda-forge python==3.10 pyyaml pandas matplotlib scikit-learn

RUN conda install -y -c conda-forge -c bioconda python=3 pyyaml pandas matplotlib scikit-learn diamond=2.1.12 blast=2.16.0

RUN pip3 install git+https://github.com/qiyunlab/HGTector.git
