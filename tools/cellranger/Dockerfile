# Set the base image to Ubuntu 16.04
FROM ubuntu:16.04

LABEL	org.opencontainers.image.authors="alex.thiery@crick.ac.uk, david.j.pearton@kcl.ac.uk" \
      description="Docker image containing cellranger"

# update apt-get and install
RUN  apt-get update \
  && apt-get install -y wget \
  && rm -rf /var/lib/apt/lists/*

# Install cellranger
RUN cd /opt/ && \
wget -O cellranger-8.0.1.tar.gz "https://cf.10xgenomics.com/releases/cell-exp/cellranger-8.0.1.tar.gz?Expires=1729288491&Key-Pair-Id=APKAI7S6A5RYOXBWRPDA&Signature=N9RJZ-yU9kPYG85iUR9im2sJUY66OgYxjGmX-cKPJui96iENOu47mnw~IR42Sb5efbaviyi5iVJNJB4D8N7k2bPPXgYwjyIDtrnL5HdKfGzg15FPCI13RIDHgy5TE7j4t3fyFeabhplQkZGD9vI6lZdJoCuA6tH1sOC7gad-FgtU-L9c2CGAFm0O~6~DknaaAf5hO~whQ5PjhF1eVQzkruqH~4me29L5Ntb7rGKwlKR~~tqhSHOTJeSRDjZPl1DFhOOVLkeHGbyGJZSlF8pIc8LbaCj-a9RSzcJ5p~u~EYs5bUgojQa-lKUgpJUoOUB7O-XgR5SLuqkNRudoai7MTQ__" && \	
	tar -xzvf cellranger-8.0.1.tar.gz && \
	rm -f cellranger-8.0.1.tar.gz

# Set path
ENV PATH /opt/cellranger-8.0.1:$PATH
