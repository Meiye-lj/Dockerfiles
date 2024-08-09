# Start from the Ruby 3 image
FROM ruby:3
# Set environment variable to noninteractive
ENV DEBIAN_FRONTEND=noninteractive
# Set the working directory
WORKDIR /maybe
# Update and install necessary packages
RUN apt-get update && apt-get install -y \
build-essential \
nodejs \
postgresql-client \
redis-server
# Expose port 3000
EXPOSE 3000
# Set the default command to run when the container is started

CMD ["/bin/bash"]
