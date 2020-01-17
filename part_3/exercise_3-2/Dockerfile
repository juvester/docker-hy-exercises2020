FROM ubuntu:18.04

ENV LC_ALL=C.UTF-8

RUN apt-get update && apt-get -y install python3-pip ffmpeg wget && \
    pip3 install --user yle-dl && \
    rm -rf /var/lib/apt/lists/*

WORKDIR /videos

ENTRYPOINT ["/root/.local/bin/yle-dl"]
