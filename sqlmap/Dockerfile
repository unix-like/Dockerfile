FROM ubuntu

RUN apt-get update && apt-get install -y \
    python2.7 \
    git \
 && rm -rf /var/lib/apt/lists/* \
 && rm -rf /var/cache/apt/archives/* \
 && git clone --depth 1 https://github.com/sqlmapproject/sqlmap.git sqlmap-dev

CMD ["python2.7","/sqlmap/sqlmap.py"]

