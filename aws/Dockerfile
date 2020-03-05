FROM frolvlad/alpine-miniconda3:python3.7

ARG CLI_VERSION=1.18.14

RUN apk add --no-cache bash
RUN conda install -c conda-forge awscli==$CLI_VERSION

WORKDIR /aws

