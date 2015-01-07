FROM debian:wheezy

RUN apt-get update && \
    apt-get install -y wget && \
    rm -rf /var/lib/apt/lists/*

RUN wget http://s3.amazonaws.com/influxdb/influxdb_latest_amd64.deb && \
    dpkg -i influxdb_latest_amd64.deb

EXPOSE 8083 8086

CMD ["influxdb", "-config", "/opt/influxdb/shared/config.toml"]
