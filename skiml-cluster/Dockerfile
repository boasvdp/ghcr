FROM mambaorg/micromamba:1.5.8-lunar

LABEL dockerfile.version="1"
LABEL software="skiml-cluster"

# RUN apt-get update && apt-get install -y \
#     git \
#     cmake \
#     build-essential \
#     libssl-dev \
#     libffi-dev \
#     python3-dev \
#     python3-pip

# RUN pip install skiml-cluster

COPY environment.yml .

RUN micromamba install -y -n base -f environment.yml