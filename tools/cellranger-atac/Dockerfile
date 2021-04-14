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
  wget -O cellranger-atac-1.2.0.tar.gz "https://cf.10xgenomics.com/releases/cell-atac/cellranger-atac-1.2.0.tar.gz?Expires=1617940351&Policy=eyJTdGF0ZW1lbnQiOlt7IlJlc291cmNlIjoiaHR0cHM6Ly9jZi4xMHhnZW5vbWljcy5jb20vcmVsZWFzZXMvY2VsbC1hdGFjL2NlbGxyYW5nZXItYXRhYy0xLjIuMC50YXIuZ3oiLCJDb25kaXRpb24iOnsiRGF0ZUxlc3NUaGFuIjp7IkFXUzpFcG9jaFRpbWUiOjE2MTc5NDAzNTF9fX1dfQ__&Signature=bzkYGbdfz2NwCseIviIgK-r9aHn7T5JrpiJVUKLfmqMJEW9iIwpD0tvQAXnTAn2J8CuF~H-q-jspcFzto0AllM24H2RSfz7K980V3aVuAU0ddNKydAhjYkO7-RJKe66v-rLiS4eGz~gXzQQmlr31XR0sZh-bwR5nKa4M4KGpUwaQhkKZsVdl7qNhVc1SfdzbynN7UExA-sIwn~FUoGn27thpxnXhF7Qjj2qw1gCexadmHFujmVVyBTKOow4IuwZsOXtB8qt~pGXRDl6Jk3z3po9RmOXiCOtQskzz3Vc~ei6EvoytoVpNJ-KWUB1bpAstLrcYr8OnUKFRqm9Ld4A7iA__&Key-Pair-Id=APKAI7S6A5RYOXBWRPDA" && \
  tar -xzvf cellranger-atac-1.2.0.tar.gz && \
	rm -f cellranger-atac-1.2.0.tar.gz

# Set path
ENV PATH /opt/cellranger-atac-1.2.0:$PATH