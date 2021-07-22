# Set the base image to miniconda
FROM continuumio/miniconda:4.7.12

LABEL authors="eva.hamrud@kcl.ac.uk" \
      description="Docker image containing cellranger-atac and python"

# update apt-get and install
RUN  apt-get update \
  && apt-get install -y wget \
  && rm -rf /var/lib/apt/lists/*

# Install cellranger-atac
RUN cd /opt/ && \
  wget -O cellranger-atac-2.0.0.tar.gz "https://cf.10xgenomics.com/releases/cell-atac/cellranger-atac-2.0.0.tar.gz?Expires=1626987944&Policy=eyJTdGF0ZW1lbnQiOlt7IlJlc291cmNlIjoiaHR0cHM6Ly9jZi4xMHhnZW5vbWljcy5jb20vcmVsZWFzZXMvY2VsbC1hdGFjL2NlbGxyYW5nZXItYXRhYy0yLjAuMC50YXIuZ3oiLCJDb25kaXRpb24iOnsiRGF0ZUxlc3NUaGFuIjp7IkFXUzpFcG9jaFRpbWUiOjE2MjY5ODc5NDR9fX1dfQ__&Signature=iTBhVwas0TXMYrWQBuAybxU~gam7bptuQqtFOXEp-wY3QeiWu58sMpKf0v6A2HZCWPNoq1pevPbSljtp6om1nwq0CG0O1aXsxHxS0K39gocHxfcDKq3qSfES5R1CalGOGN~lBT3Q4usoxSpexljZ-Y60FsvmnJEBDdruRd39-CzJPImr0por66NfwmTsytDl1sR92FoQCyENG-FuAkpTwbmHZbKCOC~14EWI2JD13gk3eUrJdXrn-n4FtXKLIQgO64GdXMzr-0sE8F5Ne2BtZzwlZExYs0srEsCz4WSt18fR6apJpKlHeQid19Owt37NjoagCLYo-EWA-ZOSR08YWA__&Key-Pair-Id=APKAI7S6A5RYOXBWRPDA" && \
  tar -xzvf cellranger-atac-2.0.0.tar.gz && \
	rm -f cellranger-atac-2.0.0.tar.gz

# Set path
ENV PATH /opt/cellranger-atac-2.0.0:$PATH