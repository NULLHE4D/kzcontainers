FROM ubuntu:20.04

WORKDIR /root
COPY ImageMagick-6.9.3-7.tar.gz /root
RUN tar -xzf ImageMagick-6.9.3-7.tar.gz

RUN DEBIAN_FRONTEND=noninteractive apt update && \
    DEBIAN_FRONTEND=noninteractive apt install -y build-essential curl

WORKDIR /root/ImageMagick-6.9.3-7
RUN ./configure && make && make install && ldconfig /usr/local/lib

WORKDIR /root
CMD bash
