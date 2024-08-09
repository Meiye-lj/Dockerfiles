FROM adoptopenjdk:11-jdk-hotspot
WORKDIR /RxJava
RUN apt-get update && apt-get install -y git
RUN git clone https://github.com/ReactiveX/RxJava.git .
RUN git checkout v3.1.8
ENV DEBIAN_FRONTEND=noninteractive
RUN apt-get update && apt-get install -y wget unzip
RUN wget https://services.gradle.org/distributions/gradle-7.0.2-bin.zip
RUN unzip -d /opt/gradle gradle-7.0.2-bin.zip
ENV GRADLE_HOME=/opt/gradle/gradle-7.0.2
ENV PATH=$PATH:$GRADLE_HOME/bin
RUN gradle build
CMD ["/bin/bash"]