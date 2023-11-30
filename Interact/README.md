# Introduction
This repository is based on [lm-design](https://github.com/facebookresearch/esm/tree/main/examples/lm-design).


# Installation

```bash
conda create -n AIGP_gj python=3.8 -y
conda activate AIGP_gj

# Install correct pytorch version for existing cuda
# I have succeeded in two versions: 1.13.1+cu117, and 2.0.0+cu118
conda install -y pytorch==1.13.1 pytorch-cuda=11.7 -c pytorch -c nvidia

# Change ./install_auto.sh for correct cuda and pytorch versions
. ./install_auto.sh
```

# Usage

```bash
CUDA_VISIBLE_DEVICES=3 python scripts/TadA_Astar_fold.py --protein 14 --keep_best 1500 --queue_size 1500 --iteration 2000000 --heuristic_evolution True --conf_threshold 0.85 --decline_rate 0.999

```