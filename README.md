
![Intro figure](https://github.com/HuguesTHOMAS/KPConv/blob/master/doc/Github_intro.png)

Created by Hugues THOMAS

## Introduction

This repository contains the implementation of **Kernel Point Convolution** (KPConv), a point convolution operator 
presented in our ICCV2019 paper ([arXiv](https://arxiv.org/abs/1904.08889)). If you find our work useful in your 
research, please consider citing:

```
@article{thomas2019KPConv,
    Author = {Thomas, Hugues and Qi, Charles R. and Deschaud, Jean-Emmanuel and Marcotegui, Beatriz and Goulette, Fran{\c{c}}ois and Guibas, Leonidas J.},
    Title = {KPConv: Flexible and Deformable Convolution for Point Clouds},
    Journal = {Proceedings of the IEEE International Conference on Computer Vision},
    Year = {2019}
}
```

**Update 03/05/2019, bug found with TF 1.13 and CUDA 10.** 
We found an internal bug inside tf.matmul operation. It returns absurd values like 1e12, leading to the 
apparition of NaNs in our network. We advise to use the code with an older version of tensorflow (TF 1.12 works well).
More info in [issue #15](https://github.com/HuguesTHOMAS/KPConv/issues/15)

## Installation

A step-by-step installation guide for Ubuntu 16.04 is provided in [INSTALL.md](./INSTALL.md). Windows is currently 
not supported as the code uses tensorflow custom operations.


## Experiments

We provide scripts for many experiments. The instructions to run these experiments are in the [doc](./doc) folder.

* [Object Classification](./doc/object_classification_guide.md): Instructions to train KP-CNN on an object classification
 task (Modelnet40).
 
* [Object Segmentation](./doc/object_segmentation_guide.md): Instructions to train KP-FCNN on an object segmentation task
 (ShapeNetPart)
 
* [Scene Segmentation](./doc/scene_segmentation_guide.md): Instructions to train KP-FCNN on several scene segmentation 
 tasks (S3DIS, Scannet, Semantic3D, NPM3D).
 
* [New Dataset](./doc/new_dataset_guide.md): Instructions to train KPConv networks on your own data.
 
* [Pretrained models](./doc/pretrained_models_guide.md): We provide pretrained weights and instructions to load them.

* Visualization of learned features (TODO).

* Visualization of learned kernel deformations (TODO).

* Visualization of Effective Receptive Fields (TODO).


## Acknowledgment

Our code uses the <a href="https://github.com/jlblancoc/nanoflann">nanoflann</a> library.

## License
Our code is released under MIT License (see LICENSE file for details).

## Updates
* 23/09/2019: Adding pretrained models for NPM3D and S3DIS dataset
* 03/05/2019: Bug found with TF 1.13 and CUDA 10
* 19/04/2019: Initial release.

