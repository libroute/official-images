# Inception v3

## Overview

Inception is a deep convolutional neural network trained on the ImageNet 2012 Challenge data set, described in [Rethinking the Inception Architecture for Computer Vision](https://arxiv.org/abs/1512.00567).

## Source code and data

This module is based on the Tensorflow tutorial repository [source code](https://github.com/tensorflow/models/blob/master/tutorials/image/imagenet/classify_image.py) which uses the model weights from the [Inception 2015-12-05](http://download.tensorflow.org/models/image/imagenet/inception-2015-12-05.tgz) file.

The implementation used within this module modifies the original to use stdin and embeds the data and code required within the image.

## Usage

To run, pass an image file (e.g. JPEG format) to the stdin of the container. The output is a list of the top 5 categories and scores for each category.

