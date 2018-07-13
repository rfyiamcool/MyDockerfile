FROM alpine:latest
MAINTAINER rfyiamcool <rfyiamcool@163.com>

ENV VERSION 1.0

RUN apk update
RUN apk add py-pip
RUN pip install --upgrade pip
RUN pip install shadowsocks

ENTRYPOINT ["/usr/bin/ssserver","--log-file=/var/log/shadowsocks.log"]
