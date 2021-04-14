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
  wget -O cellranger-atac-1.2.0.tar.gz "https://cf.10xgenomics.com/releases/cell-atac/cellranger-atac-1.2.0.tar.gz?Expires=1618438611&Policy=eyJTdGF0ZW1lbnQiOlt7IlJlc291cmNlIjoiaHR0cHM6Ly9jZi4xMHhnZW5vbWljcy5jb20vcmVsZWFzZXMvY2VsbC1hdGFjL2NlbGxyYW5nZXItYXRhYy0xLjIuMC50YXIuZ3oiLCJDb25kaXRpb24iOnsiRGF0ZUxlc3NUaGFuIjp7IkFXUzpFcG9jaFRpbWUiOjE2MTg0Mzg2MTF9fX1dfQ__&Signature=fpRycHMyUeLt~rg2L1S2~XLEkQbrZ-soPxEyLc9iIFz-~iPYmVxM6DVAy9oEqERZLpAHHS2QLZclLrzGTOUT~--eG3ZYFC0rV0I~qJZ7QOjP-8QczY55EVKgnTVnE4AHVLGVO-nwlAB99hjvtyVPoC4801z8S46L-rF9MEIdGxRkqy6oy1NNr3fB--DnTHieSQ311HbWxw1g23uN6lJHpBKJ9uqWqHrcXBW90D-OAMDSeJjcaqMSYC5pIMEmIoC~cDNuW9e1tghrD5lcnPwdyHBzPUaurrF16bX4j0oiqZsJvuHPSKilvjC3tXSuLlOtCQBjxNI59Q2gVJL38SrCDQ__&Key-Pair-Id=APKAI7S6A5RYOXBWRPDA" && \
  tar -xzvf cellranger-atac-1.2.0.tar.gz && \
	rm -f cellranger-atac-1.2.0.tar.gz

# Set path
ENV PATH /opt/cellranger-atac-1.2.0:$PATH