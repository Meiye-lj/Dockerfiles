# Use the debian:bullseye as the base image
FROM debian:bullseye

# Set the environment variable for non-interactive frontend during installation
ENV DEBIAN_FRONTEND=noninteractive

# Update package lists and install necessary build dependencies
RUN apt-get update \
&& apt-get install -y --no-install-recommends \
build-essential \
libssl-dev \
zlib1g-dev \
libncurses5-dev \
libncursesw5-dev \
libreadline-dev \
libsqlite3-dev \
libgdbm-dev \
libdb5.3-dev \
libbz2-dev \
libexpat1-dev \
liblzma-dev \
tk-dev \
libffi-dev \
wget \
ca-certificates \
git \
&& rm -rf /var/lib/apt/lists/*

# Set the working directory for cpython and clone the project from GitHub
WORKDIR /cpython
RUN git clone https://github.com/python/cpython.git . \
&& git checkout v3.13.0a4 \
&& ./configure --enable-optimizations \
&& make \
&& make install

# Set the default command to /bin/bash
CMD ["/bin/bash"]