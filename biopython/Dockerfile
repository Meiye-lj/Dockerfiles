# Dockerfile for biopython project

# Use the official Python image from the Docker Hub
FROM python:3.11

# Set non-interactive mode for apt commands
ENV DEBIAN_FRONTEND=noninteractive

# Set the working directory to /biopython
WORKDIR /biopython

# Clone the biopython project from GitHub and switch to the biopython-183 branch
RUN git clone https://github.com/biopython/biopython.git .
RUN git checkout biopython-183

# Install the Python dependencies
RUN pip install biopython

# Install the project using setup.py for development
RUN python setup.py develop

# Expose port 8080
EXPOSE 8080

# Set the command to be executed when running the container
CMD ["/bin/bash"]