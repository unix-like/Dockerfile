FROM ubuntu

RUN apt-get update && apt-get install -y \
    python2.7 \
    git \
 && rm -rf /var/lib/apt/lists/* \
 && rm -rf /var/cache/apt/archives/* \
 && git clone https://github.com/sqlmapproject/sqlmap.git

