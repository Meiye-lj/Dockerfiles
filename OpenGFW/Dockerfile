# Stage 1: Build the application
FROM golang:1.21 AS builder
ENV DEBIAN_FRONTEND=noninteractive
WORKDIR /OpenGFW
RUN git clone https://github.com/apernet/OpenGFW.git .
RUN git checkout v0.2.0
RUN go get github.com/francoispqt/gojay@v1.2.13
RUN go mod tidy
RUN go build -o OpenGFW
# Stage 2: Create a minimal container
FROM debian:buster-slim
ENV DEBIAN_FRONTEND=noninteractive
WORKDIR /app

CMD ["/bin/bash"]
