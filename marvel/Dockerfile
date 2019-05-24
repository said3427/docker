##Docker for Metagenomic Analysis and Retrieval of Viral Elements 
FROM python:3.5

# File Author / Maintainer
MAINTAINER Said Munoz Montero <said3427@gmail.com>

ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
ENV PATH /opt/conda/bin:$PATH

RUN apt-get update --fix-missing && \
    apt-get install -y wget bzip2 ca-certificates curl git && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/*


RUN pip3 install -U numpy scipy biopython scikit-learn

RUN wget --quiet https://repo.anaconda.com/miniconda/Miniconda3-4.5.11-Linux-x86_64.sh -O ~/miniconda.sh && \
    /bin/bash ~/miniconda.sh -b -p /opt/conda && \
    rm ~/miniconda.sh && \
    /opt/conda/bin/conda clean -tipsy && \
    ln -s /opt/conda/etc/profile.d/conda.sh /etc/profile.d/conda.sh && \
    echo ". /opt/conda/etc/profile.d/conda.sh" >> ~/.bashrc && \
    echo "conda activate base" >> ~/.bashrc

RUN conda install -c conda-forge -c bioconda prokka
RUN conda install -c bioconda hmmer

RUN git clone https://github.com/LaboratorioBioinformatica/MARVEL && cd MARVEL/
WORKDIR /MARVEL/
RUN	python3 download_and_set_models.py

