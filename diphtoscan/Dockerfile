FROM condaforge/mambaforge

LABEL base.image="ubuntu:mambaforge"
LABEL dockerfile.version="1"
LABEL software="diphtoscan"
LABEL software.version="1.7.0"
LABEL description="diphtOscan is a tool to search genomic assemblies of Corynebacterium diphtheriae and other species of the Corynebacterium diphtheriae species complex (CdSC)"
LABEL website="https://gitlab.pasteur.fr/BEBP/diphtoscan"

RUN apt-get update && apt-get install -y --no-install-recommends \
  tree

RUN pwd

RUN tree -L 3 /

RUN tree -L 3

RUN mamba install -c conda-forge -c bioconda python<3.12 mash==2.3 blast==2.*  ncbi-amrfinderplus==3.12.8 hmmer

RUN tree -L 3

RUN git clone https://gitlab.pasteur.fr/BEBP/diphtoscan.git

RUN tree -L 3

RUN chmod -R 777 diphtoscan/
RUN ln -s diphtoscan/__main__.py diphtoscan/diphtoscan.py

RUN tree -L 3

