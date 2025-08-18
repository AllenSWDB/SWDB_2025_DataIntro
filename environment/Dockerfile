# hash:sha256:6165b6b4f9331be970824a9bd8fb4fb8e09160cfb96c71dc8373f9c6928fddc4
ARG REGISTRY_HOST
FROM $REGISTRY_HOST/codeocean/mambaforge3:23.1.0-4-python3.10.12-ubuntu22.04

ARG DEBIAN_FRONTEND=noninteractive

ARG GIT_ASKPASS
ARG GIT_ACCESS_TOKEN
COPY git-askpass /

RUN pip3 install -U --no-cache-dir \
    aind-data-access-api==1.2.1 \
    hdmf==3.14.6 \
    hdmf-zarr==0.11.3 \
    matplotlib==3.10.1 \
    numpy==2.2.5 \
    nwbwidgets==0.11.3 \
    pandas==2.2.3 \
    pynwb==3.0.0

COPY postInstall /
RUN /postInstall
