FROM debian:wheezy

RUN apt-get update && \
    apt-get install -y python-pip && \
    rm -rf /var/lib/apt/lists/* && \
    pip install shadowsocks

CMD ["ssserver", "-c", "/server.json"]
