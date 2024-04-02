FROM rust:1.77

LABEL base.image="rust:1.77"
LABEL dockerfile.version="0"
LABEL software="distle"

RUN git clone git@github.com:KHajji/distle.git && cd distle && cargo build --release