# hash:sha256:8f899135f5a0de804a31f461c234f422fcbd58f80d37c3bfb5e37408db838734
ARG REGISTRY_HOST
FROM $REGISTRY_HOST/codeocean/py-r:python3.10.12-R4.2.2-IRkernel-ubuntu22.04

ARG DEBIAN_FRONTEND=noninteractive

ARG GIT_ASKPASS
ARG GIT_ACCESS_TOKEN
COPY git-askpass /

RUN conda install -y --channel=conda-forge --channel=bioconda \
        anndata==0.9.2 \
        leidenalg==0.10.1 \
        matplotlib==3.7.2 \
        pandas==2.0.3 \
        scanpy==1.9.5 \
    && conda clean -ya
