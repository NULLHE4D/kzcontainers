FROM ubuntu:20.04

WORKDIR /root
COPY ImageMagick-7.0.1-0.tar.gz /root
RUN tar -xzf ImageMagick-7.0.1-0.tar.gz

RUN DEBIAN_FRONTEND=noninteractive apt update && \
    DEBIAN_FRONTEND=noninteractive apt install -y build-essential curl

WORKDIR /root/ImageMagick-7.0.1-0
RUN ./configure && make && make install && ldconfig /usr/local/lib

WORKDIR /root
CMD bash
