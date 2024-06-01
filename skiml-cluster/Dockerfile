FROM condaforge/mambaforge

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
RUN /bin/bash -c "mamba env update -n base -f environment.yml"

RUN mkdir /variants && touch /variants/sampleA.vcf && touch /variants/sampleB.vcf
RUN skiml-cluster run --input /variants --output /variants_output --conda-create-envs-only
RUN rm -rf /variants