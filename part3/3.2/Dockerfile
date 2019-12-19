FROM ubuntu:16.04

WORKDIR /app

RUN apt-get update && \
    apt-get -y install curl \
    rtmpdump wget ffmpeg python3-dev python3-setuptools \
    python3-pip python3-crypto python3-requests python3-lxml \
    php-cli php-curl php-xml php-bcmath && \
    pip3 install --user --upgrade yle-dl

ENTRYPOINT ["/root/.local/bin/yle-dl"]