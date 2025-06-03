FROM continuumio/miniconda3:25.1.1-2

LABEL author="conanyangqun"
LABEL github="https://github.com/conanyangqun/container-for-bioinformatics"

RUN conda install -y -c conda-forge python==3.10 pyyaml pandas matplotlib scikit-learn

RUN pip install git+https://github.com/qiyunlab/HGTector.git
