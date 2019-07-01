# MRI_Brain_Segmentation

## Introduction

This project is to study the use of Convolutional Neural Network and in particular the ResNet architecture. The show case is segmentation of Magnetic Resonance Images (MRI) of human brain into anatomical regions[2]. We will extend the ResNet topology into the processing of 3-dimensional voxels.


## Implementation

Using Keras, we implemented a function which return a Keras model object of residual block and by calling it multiple times with desired parameters (e.g. no. of filters to use, transformation of volume between input and output), we formed a network which only takes in a 26x26x26 voxel of MRI images.

This size of voxel can carry 8 times more of information than the original 13x13x13 voxel in [2]. We have experimented our network with 2D patch input and found that it doesn’t contribute much to the accuracy so in this we discarded it to focus on training a 3D voxel residual network. We particularly employed the full pre‐activation version of residual block presented in [3], where Kaiming He found that such version offers much better training performance than the original ResNet.




## Reference


[1] Deep Residual Learning for Image Recognition

https://arxiv.org/abs/1512.03385#

[2] Deep Neural Netowrk for Anatomical Brain Segmentation

https://arxiv.org/abs/1502.02445

[3] Identity Mappings in Deep Residual Networkss

https://arxiv.org/abs/1603.05027 




