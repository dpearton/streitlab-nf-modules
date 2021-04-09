# Set the base image to Ubuntu 16.04
FROM ubuntu:16.04

LABEL authors="eva.hamrud@kcl.ac.uk" \
      description="Docker image containing cellranger-atac"

# update apt-get and install
RUN  apt-get update \
  && apt-get install -y wget \
  && rm -rf /var/lib/apt/lists/*

# Install cellranger-atac-1
RUN cd /opt/ && \
  wget -O cellranger-atac-1.2.0.tar.gz "https://cf.10xgenomics.com/releases/cell-atac/cellranger-atac-1.2.0.tar.gz?Expires=1618022849&Policy=eyJTdGF0ZW1lbnQiOlt7IlJlc291cmNlIjoiaHR0cHM6Ly9jZi4xMHhnZW5vbWljcy5jb20vcmVsZWFzZXMvY2VsbC1hdGFjL2NlbGxyYW5nZXItYXRhYy0xLjIuMC50YXIuZ3oiLCJDb25kaXRpb24iOnsiRGF0ZUxlc3NUaGFuIjp7IkFXUzpFcG9jaFRpbWUiOjE2MTgwMjI4NDl9fX1dfQ__&Signature=SqA80g7fomR0E9WwMuuTej5J5GuS9WVDy-h2iZGzlWnCWKpkgEDS7nsUanykqWWU6l7UhrMDSbxDLDrHvDvfrQZJYmXRdvsB6kD5K~HpodugRMNs-wclc4uAGRQa5uHL~rTtMGBCLtdW2Jgw61cG5wbyyZQY02bxnS4nqEOMli5X0oM~Rb-VA~sm2326F5qqAkPGfOsh4XuPpMdqzyGbf5Lm6N42MHw7uVzONraakHPA5~t-tQ9ZjTL9xgrS4eut85JsAr7egd7NBFRN4GmAX3DHMa7Gm5MklkwC8ViypcTBxyexkqDLDJ4fXUS7T7TpS9-PpLKQj0Y5CQHqVrFF3g__&Key-Pair-Id=APKAI7S6A5RYOXBWRPDA" && \
  tar -xzvf cellranger-atac-1.2.0.tar.gz && \
	rm -f cellranger-atac-1.2.0.tar.gz

# Set path
ENV PATH /opt/cellranger-atac-1.2.0.tar.gz:$PATH