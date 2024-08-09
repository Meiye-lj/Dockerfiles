# Use an official Golang runtime as a base image
FROM golang:1.21

# Set environment variable to avoid interactive prompts during package installation
ENV DEBIAN_FRONTEND=noninteractive

# Set the working directory inside the container
WORKDIR /sing-box

# Clone the project from the GitHub repository
RUN git clone https://github.com/SagerNet/sing-box.git .

# Checkout a specific version of the project
RUN git checkout v1.8.5

# Install any necessary dependencies
RUN go mod tidy && make

# Set the default command to run when the container starts
CMD ["/bin/bash"]