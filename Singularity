Bootstrap: library
From: debian:9

%environment
    export PATH=/opt/conda/bin:${PATH}

%post
	apt-get update && \
    apt-get update && apt-get -y upgrade
    apt-get -y install \
    build-essential \
    wget \
    bzip2 \
    ca-certificates \
    libglib2.0-0 \
    libxext6 \
    libsm6 \
    libxrender1 \
    git
    rm -rf /var/lib/apt/lists/*
    apt-get clean
    wget -c https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh ;\
    /bin/bash Miniconda3-latest-Linux-x86_64.sh -bfp /usr/local ;\
    conda update conda ;\
	conda install -c rdkit rdkit ;\
    conda install -c anaconda pygraphviz ;\
    conda install -c potassco clingo ;\
	pip install pathmodel

