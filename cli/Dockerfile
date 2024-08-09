# Use the official golang image for compilation
FROM golang:1.21

# Set environment variable to prevent interactive prompts during package installation
ENV DEBIAN_FRONTEND=noninteractive

# Set working directory
WORKDIR /cli

# Clone the project repository and checkout a specific version
RUN git clone https://github.com/cli/cli.git . && \
git checkout v2.43.1

# Install any necessary dependencies
# ... (if any specific system dependencies are mentioned in the documentation)

# Perform Go module tidy and build the project
RUN go mod tidy && make

# If no explicit command is mentioned, use /bin/bash as default
CMD ["/bin/bash"]