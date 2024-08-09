# Start with the base image
FROM ubuntu:latest

# Set environment variable for non-interactive front end
ENV DEBIAN_FRONTEND=noninteractive

# Set the working directory
WORKDIR /redis

# Clone the Redis repository
RUN apt update && apt install -y git
RUN git clone https://github.com/redis/redis.git .
RUN git checkout 7.2.4

# Install build dependencies
RUN apt install -y build-essential tcl

# Build Redis
RUN make

# Test Redis
RUN make test

# Expose the default port
EXPOSE 6379

# Run the Redis server with the default configuration
CMD ["/redis/src/redis-server"]