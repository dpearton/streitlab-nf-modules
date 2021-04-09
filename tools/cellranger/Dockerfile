# Set the base image to Ubuntu 16.04
FROM ubuntu:16.04

LABEL authors="alex.thiery@crick.ac.uk" \
      description="Docker image containing cellranger"

# update apt-get and install
RUN  apt-get update \
  && apt-get install -y wget \
  && rm -rf /var/lib/apt/lists/*

# Install cellranger
RUN cd /opt/ && \
	wget -O cellranger-6.0.0.tar.gz "https://cf.10xgenomics.com/releases/cell-exp/cellranger-6.0.0.tar.gz?Expires=1617939338&Policy=eyJTdGF0ZW1lbnQiOlt7IlJlc291cmNlIjoiaHR0cHM6Ly9jZi4xMHhnZW5vbWljcy5jb20vcmVsZWFzZXMvY2VsbC1leHAvY2VsbHJhbmdlci02LjAuMC50YXIuZ3oiLCJDb25kaXRpb24iOnsiRGF0ZUxlc3NUaGFuIjp7IkFXUzpFcG9jaFRpbWUiOjE2MTc5MzkzMzh9fX1dfQ__&Signature=C324pkZC3vzUkgbAv9vZoSnSBjwdv-NrH2hDKAf2noqrItOGI0hWhPmgXf-0YPcd-QrGkM2ew2c4ZuP-HcdxvgcZ1yI7RQPivR1Lt2J4u6dz2TRixHpFCeDfkDyWTgl1uaDB-JpHSRqlvJa8Tu-rnIK81VAQLodKneWCHkagU5fqKUAuiaaVGFGhTQ9WZhfE91FVE0~r-Y6717m4OMc4GybabKGoP6solVOmV9bikSppc0K4J~czlGK606PFetarkFrqd9Apqdq7I1C8RSIGUmAV2iMbCVuwPRRsVJxa-FN0k~3fVJ6sJFmcOj~2e9OQQTxv5zqWe7d0MZo~gTSTLA__&Key-Pair-Id=APKAI7S6A5RYOXBWRPDA" && \
  tar -xzvf cellranger-6.0.0.tar.gz && \
	rm -f cellranger-6.0.0.tar.gz

# Set path
ENV PATH /opt/cellranger-6.0.0:$PATH