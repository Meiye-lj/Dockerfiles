# Use a base image
FROM golang:1.21 AS build
# Set non-interactive environment
ENV DEBIAN_FRONTEND=noninteractive
# Set the working directory
WORKDIR /thanos
# Clone the project source
RUN git clone https://github.com/thanos-io/thanos.git .
# Checkout the specific version v0.34.0
RUN git checkout v0.34.0
# Install dependencies
RUN go mod tidy
# Build Thanos
RUN make build
# Create a final lightweight image
FROM alpine:3.14
# Set the command to be executed when running the container

CMD ["/bin/bash"]
