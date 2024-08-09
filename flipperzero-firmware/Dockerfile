# Use base image with required dependencies
FROM ubuntu:20.04

# Set noninteractive environment variable for Debian frontend
ENV DEBIAN_FRONTEND=noninteractive

# Set the working directory
WORKDIR /flipperzero-firmware

# Clone the project repository
RUN apt-get update && apt-get install -y git \
&& git clone https://github.com/flipperdevices/flipperzero-firmware.git . \
&& git checkout 0.98.3

# No command.

# Set the default command if not explicitly mentioned in the project
CMD ["/bin/bash"]