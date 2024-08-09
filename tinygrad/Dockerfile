FROM python:3.9
ENV DEBIAN_FRONTEND=noninteractive
WORKDIR /tinygrad
RUN git clone https://github.com/tinygrad/tinygrad.git .
RUN git checkout v0.8.0
RUN python -m pip install --upgrade pip
RUN python -m pip install --no-cache-dir -e .
CMD ["/bin/bash"]