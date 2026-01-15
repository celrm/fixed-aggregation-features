# README

Observation: this code is based on public code from the following accepted paper:

@inproceedings{
luo2024classic,
title={Classic {GNN}s are Strong Baselines: Reassessing {GNN}s for Node Classification},
author={Yuankai Luo and Lei Shi and Xiao-Ming Wu},
booktitle={The Thirty-eight Conference on Neural Information Processing Systems Datasets and Benchmarks Track},
year={2024},
url={https://openreview.net/forum?id=xkljKdGe4E}
}

Some changes have been done in main.py, parse.py, and new files aggregation_other.py, aggregation.py, model_faf.py, best_hyperparams.json.

## Dataset

Chameleon and Squirrel: one can download the datasets from the google drive link below:
https://drive.google.com/drive/folders/1rr3kewCBUvIuVxA6MJ90wzQuF-NnCRtf?usp=drive_link (provided by Qitian Wu and Wentao Zhao and Chenxiao Yang and Hengrui Zhang and Fan Nie and Haitian Jiang and Yatao Bian and Junchi Yan, Simplifying and empowering transformers for large-graph representations. In Thirty-seventh Conference on Neural Information Processing Systems, 2023b.)

Download the geom-gcn folder, place it in `./data/` and unzip it. And we use the [new splits](https://github.com/yandex-research/heterophilous-graphs/tree/main) for Chameleon and Squirrel, that filter out the overlapped nodes.
Download `chameleon_filtered.npz`, put it into `./data/geom-gcn/chameleon/`.
Download `squirrel_filtered.npz`, put it into `./data/geom-gcn/squirrel/`.
