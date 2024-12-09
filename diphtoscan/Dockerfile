FROM condaforge/mambaforge

LABEL base.image="ubuntu:mambaforge"
LABEL dockerfile.version="1"
LABEL software="diphtoscan"
LABEL software.version="1.7.0"
LABEL description="diphtOscan is a tool to search genomic assemblies of Corynebacterium diphtheriae and other species of the Corynebacterium diphtheriae species complex (CdSC)"
LABEL website="https://gitlab.pasteur.fr/BEBP/diphtoscan"

RUN mamba install \
    -c conda-forge -c bioconda \
    python==3.11.11 \
    mash==2.3 \
    blast==2.16.0 \
    ncbi-amrfinderplus==3.12.8 \
    hmmer==3.4 \
    pandas==2.2.3 \
    biopython==1.84

RUN git clone https://gitlab.pasteur.fr/BEBP/diphtoscan.git && \
    cd diphtoscan && \
    chmod -R 777 . && \
    ln -s __main__.py /usr/bin/diphtoscan && \
    diphtoscan --help
