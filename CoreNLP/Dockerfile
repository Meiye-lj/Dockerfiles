# Use a base image
FROM openjdk:11

# Set environment variable
ENV DEBIAN_FRONTEND=noninteractive

# Set working directory
WORKDIR /CoreNLP

# Clone the project from GitHub
RUN git clone https://github.com/stanfordnlp/CoreNLP.git .
RUN git checkout v4.5.6

# Update and install necessary packages
RUN apt update && apt install -y maven git

# Build the project using Maven
RUN mvn package

# Expose the default port
EXPOSE 8080

# Specify the command to be executed when the container starts
CMD ["/bin/bash"]