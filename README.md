# LMQFormer: A Laplace-Prior-Guided Mask Query Transformer for Lightweight Snow Removal <br> (Accepted by IEEE TCSVT)

<img src=".\img\result.png" alt="result" style="zoom:50%;" />


Qualitative results on synthetic datasets. From top to bottom rows: Snow100K, SRRS, CSD, SnowKitti2012 and SnowCityScapes. Please zoom in for better visual quality.

# Abstract:

Snow removal focuses on identifying snow-covered areas and restoring clean images without repairing traces. Unlike the regularity and semitransparency of rain, snow appears in various patterns and causes severe occlusion of the background. As a result, state-of-the-art snow removal methods typically require a large number of parameters. This paper introduces a lightweight yet highly efficient snow removal network called Laplace Mask Query Transformer (LMQFormer).  

First, a Laplace-VQVAE is proposed to generate a coarse mask as prior knowledge of snow. Rather than relying on predefined masks from datasets, this model aims to reduce both the information entropy of snow and the computational cost of recovery. Next, a Mask Query Transformer (MQFormer) is designed to remove snow using the coarse mask. This architecture employs two parallel encoders and a hybrid decoder to capture extensive snow features while maintaining a lightweight structure. Additionally, a Duplicated Mask Query Attention (DMQA) mechanism is introduced, converting the coarse mask into a specific number of queries that constrain the attention areas of MQFormer while reducing parameters.  

Experimental results on popular datasets demonstrate the efficiency of the proposed model, achieving state-of-the-art snow removal quality with significantly fewer parameters and the lowest running time.

[[Paper Download]]([LMQFormer: A Laplace-Prior-Guided Mask Query Transformer for Lightweight Snow Removal | IEEE Journals & Magazine | IEEE Xplore](https://ieeexplore.ieee.org/abstract/document/10092769))


# Network Architecture

<img src=".\img\network.png" alt="network" style="zoom:50%;" />


# Setup and environment

#### To generate the recovered result you need:

1. Python 3.7
2. CPU or NVIDIA GPU + CUDA CuDNN
3. Pytorch 1.8.0
4. python-opencv

#### Testing

We trained our model in five snow removal datasets, including Snow100K, SRRS, CSD, SnowKitti2012 and SnowCityScapes.

Please replace weights_dir data_dir and result_dir in test.py, and put your testset in data_dir.

#### Pre-trained model
It can be downloaded from：

Link: https://drive.google.com/drive/folders/1WiFnUh6WRIiFr7sb-h3lAcoqzi6ZyTvz?usp=sharing

# Qualcomm Ai hub
The model has been compiled and profiled in Qualcomm AI Hub to optimize its performance on specific chipsets such as QC8550. 
This ensures efficient execution by leveraging hardware acceleration and optimizing resource utilization. 
A link to Qualcomm AI Hub is also provided: https://aihub.qualcomm.com/


# Citations
Please cite this paper in your publications if it is helpful for your tasks:    

Bibtex:
```
@ARTICLE{10092769,
  author={Lin, Junhong and Jiang, Nanfeng and Zhang, Zhentao and Chen, Weiling and Zhao, Tiesong},
  journal={IEEE Transactions on Circuits and Systems for Video Technology}, 
  title={LMQFormer: A Laplace-Prior-Guided Mask Query Transformer for Lightweight Snow Removal}, 
  year={2023},
  volume={33},
  number={11},
  pages={6225-6235},
  doi={10.1109/TCSVT.2023.3264824}}

```
