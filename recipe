#!/bin/bash
# 
# Linus Pithan <linus.pithan@esrf.fr>
# 2017/10/26: initial version
# based on truatpasteurdotfr/singularity-docker-miniconda3

BootStrap: docker
From: continuumio/miniconda3

%runscript
echo "This is what happens when you run the container..."
export PATH=/opt/conda/bin:${PATH}
/bin/bash

%post
export PATH=/opt/conda/bin:${PATH}
echo "Hello from inside the container"
conda update -y conda
conda update --all
#conda list > /conda.txt
touch /`date -u -Iseconds`

%labels
MAINTAINER linupi
