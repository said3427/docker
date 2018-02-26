######################################################
# Dockerfile to build Samtools 1.7 container images
# Based on Ubuntu
#####################################################

# Set the base image to Ubuntu
FROM ubuntu:18.04

# File Author / Maintainer
MAINTAINER Said Munoz Montero

# Update the repository sources list and install samtools package
RUN apt-get update && apt-get -y install samtools=1.7-1  && apt-get clean