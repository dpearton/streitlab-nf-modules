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
  wget -O cellranger-atac-2.0.0.tar.gz "https://cf.10xgenomics.com/releases/cell-atac/cellranger-atac-2.0.0.tar.gz?Expires=1621993255&Policy=eyJTdGF0ZW1lbnQiOlt7IlJlc291cmNlIjoiaHR0cHM6Ly9jZi4xMHhnZW5vbWljcy5jb20vcmVsZWFzZXMvY2VsbC1hdGFjL2NlbGxyYW5nZXItYXRhYy0yLjAuMC50YXIuZ3oiLCJDb25kaXRpb24iOnsiRGF0ZUxlc3NUaGFuIjp7IkFXUzpFcG9jaFRpbWUiOjE2MjE5OTMyNTV9fX1dfQ__&Signature=HhvlxR0WwLwcLbEZXKyYn8cjiUpArQ5nV9bF-MEdRaU0udODm9gyl5WStogeZwcWO3N6FMM5eSbOIIJ1sK7UP6Xx~P36R7xbvtB8wB6hGw0LPoXya2d9gp~fLNKGQk4XTVrnuhgf6PvJEpemqxriXwoIZvT5-o73CjRkagP5cTH0tcSWzu-8cHqY906t0Gb8WGzn0Kb9l0MByeVVLGe1Ee~Wo-50owTTr2ankO2YI~~~2qhE9FYRfn9NHEEajvM6nQVzgo-bqmsoGIADgLCmOy8AJao9JGrXxGH9rn0AQpAmSY4nxTftu8zcdTKV5luOefcQAmvC6LfnSgY2nkBthw__&Key-Pair-Id=APKAI7S6A5RYOXBWRPDA" && \
  tar -xzvf cellranger-atac-2.0.0.tar.gz && \
	rm -f cellranger-atac-2.0.0.tar.gz

# Set path
ENV PATH /opt/cellranger-atac-2.0.0.tar.gz:$PATH