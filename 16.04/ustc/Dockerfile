FROM ubuntu:16.04

ENV TZ='Asia/Shanghai'
RUN apt-get update \
    && apt-get install -y --no-install-recommends \
        apt-transport-https \
        ca-certificates \
        tzdata \
    && sed -i "s@http://.*.ubuntu.com@https://mirrors.ustc.edu.cn@g" /etc/apt/sources.list \
    && rm -rf /var/apt/cache/*

COPY ./context/ustc /root/
