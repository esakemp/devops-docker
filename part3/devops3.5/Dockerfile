FROM alpine:3.8

ENV LC_ALL=C.UTF-8

RUN apk add --no-cache wget python \
    python2-dev py-crypto py-lxml \
    py-pip py-setuptools musl-dev\
    bash curl ffmpeg gcc make tar \
    rtmpdump libxml2-dev libxslt-dev && \
    adduser -S user && \
    pip install --upgrade pip && \
    pip install pip setuptools yle-dl

WORKDIR /yle-dl
RUN chown user .
USER user
ENTRYPOINT ["yle-dl"]
    
