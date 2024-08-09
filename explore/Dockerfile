# Use the official Ruby image as the base image
FROM ruby:2.7

# Set noninteractive environment variable
ENV DEBIAN_FRONTEND=noninteractive

# Set the working directory in the container
WORKDIR /explore

# Clone the project from GitHub
RUN git clone https://github.com/github/explore.git .
RUN git checkout main

# Copy the Gemfile to the working directory

# Install dependencies
RUN bundle install

# Run lint tests
CMD ["bundle", "exec", "rubocop"]