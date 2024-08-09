# Use an official OpenJDK runtime as a base image
FROM openjdk:8
# Set environment variable to avoid interactive prompts during package installation
ENV DEBIAN_FRONTEND=noninteractive
# Set the working directory to /tutorials
WORKDIR /tutorials
# Clone the project from the GitHub repository
RUN git clone https://github.com/eugenp/tutorials.git .
# Switch to the master branch
RUN git checkout master
# Install Maven
RUN apt-get update && apt-get install -y maven
# Build the project
RUN mvn clean package
# Specify the command to be executed when the container is started

CMD ["/bin/bash"]
