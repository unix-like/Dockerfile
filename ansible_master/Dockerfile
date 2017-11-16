FROM ubuntu

MAINTAINER xiao xing <root@unix-like.com>

RUN apt-get update && apt-get install -y \
    software-properties-common  \
 && apt-add-repository -y ppa:ansible/ansible \
 && apt-get update \
 && apt-get install -y ansible \
 && rm -rf /var/lib/apt/lists/* \
 && rm -rf /var/cache/apt/archives/*
