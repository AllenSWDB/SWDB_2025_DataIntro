# hash:sha256:a88a690b5034792e420b7250beb6821cb820237de786428b582fb137f88ee11f
ARG REGISTRY_HOST
FROM $REGISTRY_HOST/codeocean/mambaforge3:23.1.0-4-python3.10.12-ubuntu22.04

ARG DEBIAN_FRONTEND=noninteractive

ARG GIT_ASKPASS
ARG GIT_ACCESS_TOKEN
COPY git-askpass /

RUN pip3 install -U --no-cache-dir \
    aind-data-access-api==1.2.1 \
    hdmf==3.14.6 \
    hdmf-zarr \
    matplotlib==3.10.1 \
    numpy==2.2.5 \
    nwbwidgets==0.11.3 \
    pandas==2.2.3 \
    pynwb

COPY postInstall /
RUN /postInstall
