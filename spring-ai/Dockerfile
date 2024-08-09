FROM maven:3.8.3-openjdk-17
ENV DEBIAN_FRONTEND=noninteractive
WORKDIR /spring-ai
RUN git clone https://github.com/spring-projects/spring-ai.git .
RUN git checkout main
RUN mvn clean package -DskipTests
CMD ["/bin/bash"]