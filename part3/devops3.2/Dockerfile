FROM ubuntu:16.04

ENV LC_ALL=C.UTF-8

RUN apt-get update && apt-get install -y wget \
    python3 python3-pip ffmpeg rtmpdump \
    python3-pip python3-crypto python3-lxml \
    python3-setuptools python3-dev && \
    pip3 install --upgrade yle-dl && \
    rm -rf /var/lib/apt/lists/*

WORKDIR /yle-dl
ENTRYPOINT ["yle-dl"]
