FROM continuumio/miniconda3:25.1.1-2

LABEL author="conanyangqun"
LABEL github="https://github.com/conanyangqun/container-for-bioinformatics"

# stuck, maybe network?
# RUN conda install -y -c conda-forge python==3.10 pyyaml pandas matplotlib scikit-learn

RUN conda install -y -c conda-forge python pyyaml pandas matplotlib scikit-learn

RUN pip3 install git+https://github.com/qiyunlab/HGTector.git
