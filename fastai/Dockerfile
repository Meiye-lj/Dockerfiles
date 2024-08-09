FROM ubuntu:20.04
ENV DEBIAN_FRONTEND=noninteractive
WORKDIR /fastai
RUN apt-get update && \
apt-get install -y git wget && \
git clone https://github.com/fastai/fastai.git . && \
git checkout 2.7.14 && \
wget --quiet https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh -O ~/miniconda.sh && \
/bin/bash ~/miniconda.sh -b -p /opt/conda && \
rm ~/miniconda.sh
ENV PATH="/opt/conda/bin:${PATH}"
RUN conda install -c fastai pytorch torchvision torchaudio cpuonly -c pytorch -y
RUN conda install -c fastai fastai -y
RUN python setup.py develop
CMD ["/bin/bash"]