# Use a base image containing Java 8
FROM openjdk:8-jdk
# Set environment variable for non-interactive frontend
ENV DEBIAN_FRONTEND=noninteractive
# Set the working directory to /nacos
WORKDIR /nacos
# Clone the Nacos project from GitHub and checkout the specific version
RUN git clone https://github.com/alibaba/nacos.git . \
&& git checkout 2.3.0
# Install Maven
RUN apt update && apt install -y maven
# Build Nacos from source
RUN mvn -Prelease-nacos -Dmaven.test.skip=true clean install -U
# Expose the ports
EXPOSE 8848 8080 8847 8808 30000 3306 8086 9200 8809 8849 8807
# Start Nacos server with standalone mode

CMD ["/bin/bash"]
