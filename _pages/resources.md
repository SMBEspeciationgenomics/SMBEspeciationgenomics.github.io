---
title: "Resources"
layout: single
permalink: /resources/
header:
  image: /images/workshop_logo.png
---

# Introduction

During the SMBE Satellite workshop on speciation genomics, we ran four practical sessions on two important software packages.

## Efficient and fast simulations with `msprime`

The first package was `msprime` and a focus on how the tree sequence format is an efficient means of storing and simulating data. New developments with `tskit` mean that it also simpler than ever to rapidly estimate summary statistics from simulated data. You can learn more about `msprime` and `tskit` [here](https://msprime.readthedocs.io/en/stable/) and [here](https://tskit.readthedocs.io/en/latest/). These sessions were led by Georgia Tsambos and Jerome Kelleher.

## Going further with genome scans using `gIMble`

The second package was `gIMble` a tool for inferring demography and effective migration rate from genome scan data. These sessions were led by Konrad Lohse, Gertjan Bischop, Derek Setter and Dom Laetsch. You can learn more about `gIMble` [here](https://github.com/DRL/gIMble).

# Using the resources

Even if you didn't attend the workshop, we want the resources to be freely available to the community. There are several ways that you can use them.

## Running the Jupyter notebooks using binder

The simplest way to get your hands on the resources is to use `binder` which will run the Jupyter notebooks we used for the workshop. Compute resources will be limited in comparison to the original run through in the workshop but you should be able to work through most of the exercises.

To run the `binder` based resources, go [here](https://github.com/DRL/SMBE-SGE-2019) and click on the launch `binder` button. Many thanks to Ariella Gladstein for making  this possible.

## Running the resources locally

Alternatively you can install the programmes locally and run the resources on your own machine. The best way to do this is via a `conda` installation but you can also install it directly using `pip`. See [here] (https://msprime.readthedocs.io/en/stable/installation.html) for more info.

You will also need to install `tskit`. This can be done via `pip` - see [here](https://tskit.readthedocs.io/en/latest/installation.html) for more info.

To install `gIMble` you will need a `conda` installation (see [here](https://docs.conda.io/en/latest/) if you are not yet familiar with the wonderful world of `conda`) and should enter the following commands:

```bash
# clone repository
git clone https://github.com/DRL/gimble.git

# create conda enviroment with dependencies
conda create -n gimble && \
source activate gimble && \
conda install -c conda-forge more-itertools tqdm scipy numpy matplotlib sympy giac networkx psutil pandas docopt pytables tabulate git htop && \
conda install -c bioconda pysam
```

You will also need `blocktools`. Again follow these commands:

```bash
# clone repository
git clone https://github.com/DRL/blocktools.git

# create conda enviroment with dependencies
conda env install -f $BLOCKTOOLS_PATH/blocktools.conda.yml

# Activate blocktools conda environment
conda activate blocktools
```

Finally, you will need to clone the github repository where the resources are stored. To do this, do the following:

```bash
git clone https://github.com/DRL/SMBE-SGE-2019.git
```

Enjoy!
