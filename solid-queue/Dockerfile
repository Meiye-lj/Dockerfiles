# Use the official Ruby image with version 3.0
FROM ruby:3.0
# Set environment variable to avoid interactive prompts during image build
ENV DEBIAN_FRONTEND=noninteractive
# Set the working directory to /solid_queue
WORKDIR /solid_queue
# Update and install dependencies
RUN apt-get update && \
apt-get install -y git
# Clone the project repository from GitHub
RUN git clone https://github.com/basecamp/solid_queue.git .
# Switch to the main branch
RUN git checkout main
# Copy the Gemfile and Gemfile.lock to the container
# Install required gems
RUN bundle install
# Expose the necessary ports
EXPOSE 3000
#

CMD ["/bin/bash"]
