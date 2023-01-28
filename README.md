# MonotonicIQA
## Table of Contents
<ul>
    <li><a href="#Model-Overview">Model Overview</a></li>
    <li><a href="#Requirement">Requirement</a></li>
    <li><a href="#Getting-Started">Getting Started</a></li>
    <li><a href="#Download">Download</a></li>
    <li><a href="#Citation">Citation</a></li>
</ul>

## Model Overview
<img width="1600" alt="image" src="https://github.com/SuperBruceJia/MonotonicIQA/blob/main/Fig/Fig2.png">

## Requirement
Python 3+<br>
PyTorch 1.4+<br>
MATLAB<br>
Successfully tested on Ubuntu 20.04

## Getting Started
### Sampling Images
[MATLAB] Sampling images from each datasets
```shell
sample_name.m
```

### Mixing Images
[MATLAB] Mixing all the sampled images
```shell
combine_pmtrain.m
```

### Train on Mixed Datasets
```shell
python Main.py --train True --network basecnn --representation BCNN --batch_size 32 --image_size 384 --lr 3e-4 --decay_interval 3 --decay_ratio 0.9 --max_epochs 24 --backbone resnet34
```

### Get Scores
```shell
python Main.py --train False --get_scores True
```

### Result Analysis
```shell
calculate_mean.m
```

## Download
Original Paper: [Link](https://ietresearch.onlinelibrary.wiley.com/doi/epdf/10.1049/ell2.12698?download=true)<br>
Proof of the Transformer: [Link](https://github.com/SuperBruceJia/MonotonicIQA/blob/main/%5BProof%5D%20Proof%20of%20the%20Transformer.pdf)

## Citation
```bibtex
@article{feng2023learning,
  title     = {Learning from Mixed Datasets: A Monotonic Image Quality Assessment Model},
  author    = {Feng, Zhaopeng and Zhang, Keyang and Jia, Shuyue and Chen, Baoliang and Wang, Shiqi},
  journal   = {IET Electronics Letters},
  volume    = {59},
  number    = {3},
  pages     = {e12698},
  year      = {Jan. 2023},
  publisher = {Wiley Online Library}
}
```
