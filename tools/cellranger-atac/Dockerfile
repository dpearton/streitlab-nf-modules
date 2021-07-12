# Set the base image to Ubuntu 16.04
FROM ubuntu:16.04

LABEL authors="eva.hamrud@kcl.ac.uk" \
      description="Docker image containing cellranger-atac"

# update apt-get and install
RUN  apt-get update \
  && apt-get install -y wget \
  && rm -rf /var/lib/apt/lists/*

# Install cellranger-atac
RUN cd /opt/ && \
  wget -O cellranger-atac-2.0.0.tar.gz "https://cf.10xgenomics.com/releases/cell-atac/cellranger-atac-2.0.0.tar.gz?Expires=1626152199&Policy=eyJTdGF0ZW1lbnQiOlt7IlJlc291cmNlIjoiaHR0cHM6Ly9jZi4xMHhnZW5vbWljcy5jb20vcmVsZWFzZXMvY2VsbC1hdGFjL2NlbGxyYW5nZXItYXRhYy0yLjAuMC50YXIuZ3oiLCJDb25kaXRpb24iOnsiRGF0ZUxlc3NUaGFuIjp7IkFXUzpFcG9jaFRpbWUiOjE2MjYxNTIxOTl9fX1dfQ__&Signature=fg-hQJISjUVi2NH~rRCaVSuS4gIZVwSkgQ6gb7TWemwaF9YyfZTf9fDz6KVMzGvMhB3XxShR9JI5CTnQWHUXDkIGyZEct2mn17hld15xre1KcY5YU4QGzz0ubx6vuNR7JdXdeBvJDs9AFA1pgSLzPCJjJ3ootLbzkyrNLW9PTblXDDDWz5lG8bTGr6EOy1dy70cH1K7EKrzmRa~9~IbdLNZuX-Ws~etS76WuLCpbSAU0oO1BK7PBZ9W2Fy7npNHnTk0xT0QuETTRSi2mzdsRZ60~2q5IUVBtW3PqxnSEYGNMwws-i81o4sNW45iVA~eq-B49pA5-K02OSB6orGPn~Q__&Key-Pair-Id=APKAI7S6A5RYOXBWRPDA" && \
  tar -xzvf cellranger-atac-2.0.0.tar.gz && \
	rm -f cellranger-atac-2.0.0.tar.gz

# Set path
ENV PATH /opt/cellranger-atac-2.0.0:$PATH