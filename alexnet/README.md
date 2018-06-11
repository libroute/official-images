# Alexnet

## Overview

Alexnet is a deep convolutional neural network which won the [ILSVRC2012 competition](http://www.image-net.org/challenges/LSVRC/2012/).

## Source code and data

The original [Caffe model](https://github.com/BVLC/caffe/tree/master/models/bvlc_alexnet) is [implemented in Tensorflow](http://www.cs.toronto.edu/%7Eguerzhoy/tf_alexnet/).

The implementation used within this module modifies the original to use stdin and embeds the data and code required within the image.

## Usage

To run, pass an image file (e.g. JPEG format) which must have dimensions 227x227x3 to the stdin of the container. The output contains the top 5 categories and scores for each category.

