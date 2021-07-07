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
  wget -O cellranger-atac-2.0.0.tar.gz "https://cf.10xgenomics.com/releases/cell-atac/cellranger-atac-2.0.0.tar.gz?Expires=1625689039&Policy=eyJTdGF0ZW1lbnQiOlt7IlJlc291cmNlIjoiaHR0cHM6Ly9jZi4xMHhnZW5vbWljcy5jb20vcmVsZWFzZXMvY2VsbC1hdGFjL2NlbGxyYW5nZXItYXRhYy0yLjAuMC50YXIuZ3oiLCJDb25kaXRpb24iOnsiRGF0ZUxlc3NUaGFuIjp7IkFXUzpFcG9jaFRpbWUiOjE2MjU2ODkwMzl9fX1dfQ__&Signature=QN8P~rlzoHZkondVP8NyCayUFrIgn11ryeqd6tQo6gF0XbK-jOjPhqyv-V1A6orz0x~fdvCJu9-ay97baS4PYiEolx~x55IbFHwZAeKmbfGRzScAHb2uJBNUJFsQR7hzGFTjvR97W0Yjjfl5npFd5-G-cVSyeDCDs9q8lywGrvYodXMnkikpYkGzVLpSCOFrrHfu3iFu8KQTbwspZSFfRyV9q46g86jOhhIKtLw3TvxYwUCG9~cHRLFfz-NdCKwZ0vq-3r34HIMY-SYIno7j~yVbIeXvAH5gYi1dokPahNWhrZOmQMieovjAcIF8AFymg7Y7Rqyor3FrSV6ErjDVBw__&Key-Pair-Id=APKAI7S6A5RYOXBWRPDA" && \
  tar -xzvf cellranger-atac-2.0.0.tar.gz && \
	rm -f cellranger-atac-2.0.0.tar.gz

# Set path
ENV PATH /opt/cellranger-atac-2.0.0.tar.gz:$PATH