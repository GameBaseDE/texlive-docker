FROM ubuntu:eoan
LABEL maintainer="ngehrsitz"
ARG DEBIAN_FRONTEND=noninteractive
RUN apt-get update && apt-get install -y \
    texlive-full \
    texlive-luatex \
    texlive-extra-utils \
    texlive-lang-german \
    xindy \
    biber \
    python-pygments gnuplot \
    openjdk-11-jre-headless
WORKDIR /texbuild
RUN adduser --disabled-password --gecos '' texbuilder
RUN chown texbuilder:texbuilder /texbuild
USER texbuilder
