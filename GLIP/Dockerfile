# Use an official Python runtime as a base image
FROM python:3.7

# Set environment variables for non-interactive frontend during installation
ENV DEBIAN_FRONTEND=noninteractive

# Set the working directory in the container
WORKDIR /GLIP

# Clone the project repository from GitHub
RUN git clone https://github.com/microsoft/GLIP.git .
RUN git checkout main

# Install required Python dependencies
RUN pip install einops shapely timm yacs tensorboardX ftfy prettytable pymongo transformers

# Install additional dependencies for the project
RUN python setup.py develop

# Expose the default port
EXPOSE 8080

# Set the default command to be executed when running the container
CMD ["/bin/bash"]