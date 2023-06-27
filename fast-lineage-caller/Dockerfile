FROM python:3.7.17-bookworm

LABEL base.image="docker-python"
LABEL dockerfile.version="1"
LABEL software="fast-lineage-caller"
LABEL software.version="0.3.1"
LABEL description="Software to identify Mtb lineage"

RUN python -m pip --version

RUN pip install fast-lineage-caller
