FROM ubuntu:18.04
RUN apt-get update
RUN apt-get install -y cmake git build-essential
RUN useradd -ms /bin/bash bioit
USER bioit
WORKDIR /home/bioit
RUN cd /home/bioit/
RUN git clone https://github.com/SuperElastix/SimpleElastix
RUN mkdir /home/bioit/build
RUN cd /home/bioit/build
RUN cmake /home/bioit/SimpleElastix/SuperBuild
RUN make -j4
