[![DOI](https://zenodo.org/badge/779008229.svg)](https://zenodo.org/doi/10.5281/zenodo.10892431)

# LLMCompass

This repository provides the implementation of **LLMCompass** from the following papers:

[**LLMCompass: Enabling Efficient Hardware Design for Large Language Model Inference**](https://parallel.princeton.edu/papers/isca24_llmcompass.pdf)

*Hengrui Zhang, August Ning, Rohan Baskar Prabhakar, David Wentzlaff*


In the Proceedings of the 51st Annual International Symposium on Computer Architecture:

```
@inproceedings{LLMCompass,
author = {Zhang, Hengrui and Ning, August and Prabhakar, Rohan Baskar and Wentzlaff, David},
title = {LLMCompass: Enabling Efficient Hardware Design for Large Language Model Inference},
year = {2024},
booktitle = {Proceedings of the 51st Annual International Symposium on Computer Architecture},
}
```


## Set up the environment

```
$ conda create -n llmcompass_ae python=3.9
$ conda activate llmcompass_ae
$ pip install scalesim
$ conda install pytorch==2.0.0 -c pytorch
$ pip3 install matplotlib
$ pip3 install seaborn
$ pip3 install scipy
$ pip3 install --pre torch torchvision torchaudio --index-url https://download.pytorch.org/whl/nightly/cpu
```

## Installation

### If using Github
```
$ git clone -b ISCA_AE https://github.com/PrincetonUniversity/LLMCompass
$ cd LLMCompass
$ git submodule init
$ git submodule update --recursive
```

### If using Zenodo
Unzip the file and download from https://github.com/PrincetonUniversity/ttm-cas.git as `cost_model\supply_chain`


### If using Docker
A Dockerfile has been provided (`./Dockerfile`), including all the software dependencies and the LLMCompass source code.

A docker image has been provided [here](https://github.com/HenryChang213/LLMCompass_ISCA_AE_docker).

## AE Experiment workflow
```
# Figure 5 (around 100 min) 
$ cd ae/figure5
$ bash run_figure5.sh 

# Figure 6 (around 1 min)
$ cd ae/figure6
$ bash run_figure6.sh

# Figure 7 (around 20 min)
$ cd ae/figure7
$ bash run_figure7.sh

# Figure 8 (around 40 min)
$ cd ae/figure8
$ bash run_figure8.sh

# Figure 9 (around 30 min)
$ cd ae/figure9
$ bash run_figure9.sh

# Figure 10 (around 45 min)
$ cd ae/figure10
$ bash run_figure10.sh

# Figure 11 (around 5 min) 
$ cd ae/figure11
$ bash run_figure11.sh

# Figure 12 (around 4 hours) 
$ cd ae/figure12
$ bash run_figure12.sh
```

## AE Expected result

After running each script above, the corresponding figures
will be generated under the corresponding directory as suggested by its name.

For comparison, a copy of the expected results can be found in `ae\expected_results`


## User Guide

A guide on "How to Run a LLMCompass Simulation" is shown [here](./docs/run.md).
