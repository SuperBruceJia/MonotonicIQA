# MonotonicIQA

Original Paper: [Link](https://github.com/SuperBruceJia/MonotonicIQA/blob/main/%5BPaper%5D%20Learning%20from%20Mixed%20Datasets-%20A%20Monotonic%20Image%20Quality%20Assessment%20Model.pdf)

Proof of the Transformer: [Link](https://github.com/SuperBruceJia/MonotonicIQA/blob/main/%5BProof%5D%20Proof%20of%20the%20Transformer.pdf)

<img width="1600" alt="image" src="https://github.com/SuperBruceJia/MonotonicIQA/blob/main/Fig/Fig2.png">

# Requirements:

Python 3+

PyTorch 1.4+

Matlab

Successfully tested on Ubuntu 20.04

# Usage

Sampling images from each datasets(Matlab)

```shell
sample_name.m
```

Mixing all the sampled images (Matlab)

```shell
combine_pmtrain.m
```

## Train on the mixed datasets for 10 sessions

```shell
python Main.py --train True --network basecnn --representation BCNN --batch_size 32 --image_size 384 --lr 3e-4 --decay_interval 3 --decay_ratio 0.9 --max_epochs 24 --backbone resnet34
```

## Get scores

```shell
python Main.py --train False --get_scores True
```

## Result analysis

```shell
calculate_mean.m
```
