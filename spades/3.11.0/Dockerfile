############################################################
# Dockerfile to build SPAdes container images
# Based on Ubuntu
############################################################

# Set the base image to Ubuntu
FROM ubuntu:18.04

# File Author / Maintainer
MAINTAINER Said Munoz Montero

# Update the repository sources list
RUN apt-get update

# Install compiler and perl stuff
RUN apt-get install --yes wget python

# Get source code
WORKDIR /tools/

RUN wget -q https://github.com/ablab/spades/releases/download/v3.11.0/SPAdes-3.11.0-Linux.tar.gz 

RUN tar -xvzf SPAdes-3.11.0-Linux.tar.gz

WORKDIR /tools/SPAdes-3.11.0-Linux

ENV PATH="/tools/SPAdes-3.11.0-Linux/bin:${PATH}"

WORKDIR /root
