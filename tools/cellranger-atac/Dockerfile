# Set the base image to Ubuntu 16.04
FROM python

LABEL authors="eva.hamrud@kcl.ac.uk" \
      description="Docker image containing cellranger-atac"

# update apt-get and install
RUN  apt-get update \
  && apt-get install -y wget \
  && rm -rf /var/lib/apt/lists/*

# Install cellranger-atac
RUN cd /opt/ && \
  wget -O cellranger-atac-2.0.0.tar.gz "https://cf.10xgenomics.com/releases/cell-atac/cellranger-atac-2.0.0.tar.gz?Expires=1622060043&Policy=eyJTdGF0ZW1lbnQiOlt7IlJlc291cmNlIjoiaHR0cHM6Ly9jZi4xMHhnZW5vbWljcy5jb20vcmVsZWFzZXMvY2VsbC1hdGFjL2NlbGxyYW5nZXItYXRhYy0yLjAuMC50YXIuZ3oiLCJDb25kaXRpb24iOnsiRGF0ZUxlc3NUaGFuIjp7IkFXUzpFcG9jaFRpbWUiOjE2MjIwNjAwNDN9fX1dfQ__&Signature=bZQWuZSF7rOnbyBdmChSCLxjFY~1FLd6KojKwPHRVgX5R5jqkj4xuNcf1I0vQCfcLaBN4z1-sJsJsFcbP27OkXN~l8fe661ALwtvfdD7FPmtEzvHEdNpQvxCwY-Y0XWjzfzOvf5l9OuVEx6p6ckvnB~X1El99QIK8OEp8~us1vozwzzHQL1Pw-JgdDe8w5u63ObknUVjyMpkNrsX7C4BHiocCwq48iuf9nA-CnbIrESRL-Y2CyoRLmz-Vs9-hvOH2UECkCVzUgreGH7wvKweuQskFG1tAyltWAhNRw5a6MzWBGR0rEEvlW-xWdFnRYVcjL9lwn3mRU7WnXTy53wygQ__&Key-Pair-Id=APKAI7S6A5RYOXBWRPDA" && \
  tar -xzvf cellranger-atac-2.0.0.tar.gz && \
	rm -f cellranger-atac-2.0.0.tar.gz

# Set path
ENV PATH /opt/cellranger-atac-2.0.0.tar.gz:$PATH