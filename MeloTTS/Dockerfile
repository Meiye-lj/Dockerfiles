# Use the official image as a base
FROM python:3.9
# Set noninteractive mode for apt
ENV DEBIAN_FRONTEND=noninteractive
# Set working directory
WORKDIR /MeloTTS
# Clone the project source code and checkout version v0.1.2
RUN git clone https://github.com/myshell-ai/MeloTTS.git .
RUN git checkout v0.1.2
# Specify the port to expose (if required)
EXPOSE 8080
# Install project dependencies
RUN pip install --no-cache-dir -r requirements.txt
RUN python setup.py develop
# Set the default command for the container

CMD ["/bin/bash"]