# Use the official golang image for the build process
FROM golang:latest

# Set noninteractive Debian frontend
ENV DEBIAN_FRONTEND=noninteractive

# Set the working directory
WORKDIR /templ

# Clone the project repository and checkout a specific version
RUN git clone https://github.com/a-h/templ.git . \
&& git checkout v0.2.543

# Copy the source code from the current directory to the Working Directory inside the container

# Perform go mod tidy to ensure clean modules
RUN go mod tidy

# Set the default command to execute when the container starts
CMD ["/bin/bash"]