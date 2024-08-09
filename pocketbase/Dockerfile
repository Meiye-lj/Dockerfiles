FROM golang:1.22
ENV DEBIAN_FRONTEND=noninteractive
WORKDIR /pocketbase
RUN git clone https://github.com/pocketbase/pocketbase.git .
RUN git checkout v0.22.3
RUN go mod tidy
RUN go build ./...
EXPOSE 8080

CMD ["/bin/bash"]
