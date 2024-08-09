# Use the official golang image as the base image
FROM golang:latest

# Set non-interactive environment for Debian
ENV DEBIAN_FRONTEND=noninteractive

# Set the working directory inside the container
WORKDIR /trufflehog

# Clone the project from the GitHub repository
RUN git clone https://github.com/trufflesecurity/trufflehog.git .

# Checkout a specific version of the project
RUN git checkout v3.67.6

# Expose port 8080
EXPOSE 8080

# Perform go module tidy
RUN go mod tidy

# Compile the code
RUN make

# Set the default command to execute when the container starts
CMD ["/bin/bash"]