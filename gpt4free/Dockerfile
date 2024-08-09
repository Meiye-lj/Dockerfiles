# Use the official Python image as base image
FROM python:3.10-slim
# Set the working directory inside the container
WORKDIR /gpt4free
# Set environment variable to avoid interactive prompts during package installation
ENV DEBIAN_FRONTEND=noninteractive
# Clone the project repository and checkout the specified version
RUN apt-get update && apt-get install -y git \
&& git clone https://github.com/xtekky/gpt4free.git . \
&& git checkout 0.2.1.3 \
&& apt-get remove -y git \
&& apt-get autoremove -y \
&& rm -rf /var/lib/apt/lists/*
# Install the necessary dependencies for the Python project
RUN pip install -r requirements.txt
RUN python setup.py develop
# Set the default command when the container starts

CMD ["/bin/bash"]
