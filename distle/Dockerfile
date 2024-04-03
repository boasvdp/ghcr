FROM rust:1.77 as builder

RUN git clone --depth 1 https://github.com/KHajji/distle.git && cd distle && cargo build --release

FROM ubuntu:jammy as app

LABEL base.image="rust:1.77"
LABEL dockerfile.version="1"
LABEL software="distle"
LABEL website="https://github.com/KHajji/distle"

COPY --from=builder /distle/target/release /usr/local/bin

WORKDIR /data

CMD ["distle --help"]

