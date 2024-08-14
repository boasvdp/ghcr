from python:3.8.19-slim

LABEL base.image="python/3.8.19-slim"
LABEL dockerfile.version="1"
LABEL software="SNP-it"
LABEL software.version="1.0.0"
LABEL description="SNP-it for MTB lineage classification"
LABEL website="https://github.com/philipwfowler/snpit"

RUN apt-get update && apt-get install --no-install-recommends -y \
    wget \
    ca-certificates \
    make \
    bzip2 \
    autoconf \
    automake \
    make \
    gcc \
    perl \
    zlib1g-dev \
    libbz2-dev \
    liblzma-dev \
    libcurl4-gnutls-dev \
    libssl-dev \
    procps && \
    rm -rf /var/lib/apt/lists/* && apt-get autoclean

RUN git clone https://github.com/philipwfowler/snpit.git && \
  cd snpit && \
  python3 setup.py install