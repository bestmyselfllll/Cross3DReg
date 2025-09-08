# Cross3DReg

Zongyi Xu, Zhongpeng Lang, Yilong Chen, Shanshan Zhao, Xiaoshui Huang, Yifan Zuo, Yan Zhang, Qianni Zhang, Xinbo Gao

## Introduction

Cross-source point cloud registration, which aims to align point cloud data from different sensors, is a fundamental task in 3D vision. However, compared to the same-source point cloud registration, cross-source registration faces two core challenges: the lack of publicly available large-scale real-world datasets for training the deep registration models, and the inherent differences in point clouds captured by multiple sensors. The diverse patterns induced by the sensors pose great challenges in robust and accurate point cloud feature extraction and matching, which negatively influence the registration accuracy. To advance research in this field, we construct Cross3DReg, the currently largest and real-world multi-modal cross-source point cloud registration dataset, which is collected by a rotating mechanical lidar and a hybrid semi-solid-state lidar, respectively. Moreover, we design an overlap-based cross-source registration framework, which utilizes unaligned images to predict the overlapping region between source and target point clouds, effectively filtering out redundant points in the irrelevant regions and significantly mitigating the interference caused by noise in non-overlapping areas. Then, a visual-geometric attention guided matching module is proposed to enhance the consistency of cross-source point cloud features by fusing image and geometric information to establish reliable correspondences and ultimately achieve accurate and robust registration. Extensive experiments show that our method achieves state-of-the-art registration performance.

![](assets/frame.PNG)

## Installation

Please use the following command for installation.

```bash
# It is recommended to create a new environment
conda create -n name python==3.8
conda activate name

# [Optional] If you are using CUDA 11.0 or newer, please install `torch==1.7.1+cu110`
pip install torch==1.7.1+cu110 -f https://download.pytorch.org/whl/torch_stable.html

# Install packages and other dependencies
pip install -r requirements.txt
python setup.py build develop
```

Code has been tested with Ubuntu 20.04, GCC 9.3.0, Python 3.8, PyTorch 1.7.1, CUDA 11.1 and cuDNN 8.1.0.

## Cross3D
The Cross3D dataset can be downloaded from the [Cross3D](https://drive.google.com/file/d/1sEvQQYLJz7reggiM08GXg2Zatck2GLft/view?usp=sharing). The partial data visualization results are shown as follow:
![](assets/visual.png)
