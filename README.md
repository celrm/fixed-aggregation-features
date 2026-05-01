# Fixed Aggregation Features Can Rival GNNs (ICML 2026)

[![arXiv](https://img.shields.io/badge/arXiv-2601.19449-b31b1b.svg)](https://arxiv.org/abs/2601.19449)
[![ICML](https://img.shields.io/badge/ICML-2026-orange.svg)](https://openreview.net/forum?id=gSZhNPp103)

>Celia Rubio-Madrigal, Rebekka Burkholz.
>CISPA Helmholtz Center for Information Security.

This repository contains the code for the paper "Fixed Aggregation Features Can Rival GNNs".

#### Abstract

>Graph neural networks (GNNs) are widely believed to excel at node representation learning through trainable neighborhood aggregations. We challenge this view by introducing Fixed Aggregation Features (FAFs), a training-free approach that transforms graph learning tasks into tabular problems. This simple shift enables the use of well-established tabular methods, offering strong interpretability and the flexibility to deploy diverse classifiers. Across 14 benchmarks, well-tuned multilayer perceptrons trained on FAFs rival or outperform state-of-the-art GNNs and graph transformers on 12 tasks—often using only mean aggregation. The only exceptions are the Roman Empire and Minesweeper datasets, which typically require unusually deep GNNs. To explain the theoretical possibility of non-trainable aggregations, we connect our findings to Kolmogorov–Arnold representations and discuss when mean aggregation can be sufficient. In conclusion, our results call for (i) richer benchmarks benefiting from learning diverse neighborhood aggregations, (ii) strong tabular baselines as standard, and (iii) employing and advancing tabular models for graph data to gain new insights into related tasks.

## Environment

Tested with Python 3.7, PyTorch 1.12.1, and PyTorch Geometric 2.3.1, dgl 1.0.2.

```bash
pip install pandas
pip install scikit_learn
pip install numpy
pip install scipy
pip install einops
pip install ogb
pip install pyyaml
pip install googledrivedownloader
pip install networkx
pip install gdown
pip install matplotlib
```

## Datasets

One can download the datasets Chameleon and Squirrel from the Google Drive link below:
https://drive.google.com/drive/folders/1rr3kewCBUvIuVxA6MJ90wzQuF-NnCRtf?usp=drive_link 

Provided by: Qitian Wu and Wentao Zhao and Chenxiao Yang and Hengrui Zhang and Fan Nie and Haitian Jiang and Yatao Bian and Junchi Yan, Simplifying and empowering transformers for large-graph representations. In Thirty-seventh Conference on Neural Information Processing Systems, 2023.

Download the geom-gcn folder, place it in `./data/` and unzip it. And we use the [new splits](https://github.com/yandex-research/heterophilous-graphs/tree/main) for Chameleon and Squirrel that filter out the overlapped nodes.
Download `chameleon_filtered.npz`, put it into `./data/geom-gcn/chameleon/`.
Download `squirrel_filtered.npz`, put it into `./data/geom-gcn/squirrel/`.


## Origin
This repository is based on [public code](https://github.com/LUOyk1999/tunedGNN) from the following accepted paper: Yuankai Luo and Lei Shi and Xiao-Ming Wu, Classic GNNs are Strong Baselines: Reassessing GNNs for Node Classification. In The Thirty-eight Conference on Neural Information Processing Systems Datasets and Benchmarks Track, 2024.

* Some changes have been done to: `main.py`, `parse.py`.
* New files are: `aggregation.py`, `aggregation_other.py`, `model_faf.py`, `best_hyperparams.json`.

## Citation

If you found this work helpful, please consider citing our paper:

```bibtex
@inproceedings{
rubio-madrigal2026fixed,
title={Fixed Aggregation Features Can Rival {GNN}s},
author={Celia Rubio-Madrigal and Rebekka Burkholz},
booktitle={Forty-third International Conference on Machine Learning},
year={2026},
url={https://openreview.net/forum?id=gSZhNPp103}
}
```

