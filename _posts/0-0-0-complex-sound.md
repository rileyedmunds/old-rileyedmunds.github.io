---
layout: post
title: Complex Sound Research
date: 2016-12-15 5:01:42
---

Update: As of December 1st, the complex valued network is functional. We have completed the pre-processing pipeline, tested on real valued data, and complex-valued data. 

We found that incorporating phase leads to significant overfitting, so to reduce this effect, we will be augmenting our dataset and writing a complex dropout Caffe layer.

Over winter break, we will also be working on our paper, **'Complex Convolutional Neural Networks for Environmental Sound Classification.'**

*[Prepublication]* Abstract: *In this paper we introduce a new framework and approach for convolutional neural network computation. By introducing layer functions that intelligently process complex-domain data in deep neural network architectures, we improve upon prior understanding and performance in complex-valued convolutional neural networks. Using novel derivations of convolutional, down-sampling, non-linear, and affine layers implemented in a complex-valued counterpart to Caffe, we proved results when evaluated against real-valued models in the context of environmental sound classification. Finally, we demonstrated these results are applicable to many other fields, including, but not limited to MRI imaging, signal processing, and LiDAR mapping.*

![paper](https://raw.githubusercontent.com/rileyedmunds/rileyedmunds.github.io/master/images/paper.png)


---

Original Post:

This semester I'm writing a paper on complex-valued convolutional neural networks. Here's the big idea:

Some data carry critical information in the complex domain. However, popular frameworks have effectively no support for complex-valued data.

What if we could train not only on magnitudes of pixel gradients and sounds, but also their relative phases?


1. Why do we want to incorporate phase?

In many types of data (MRI imaging data, musical data, low frequency sound data) there seems to be vital information encoded in the complex domain.

2. What challenges do we face when training CNNs on complex numbers?

Complex numbers are difficult to think about. What does it mean to threshold a complex number? What effect does a gaussian kernel have on backgropagation? How do you convolve pixel gradients or phase? Which activation functions are both meaningful in the complex domain and holomophic?

3. How do we plan on testing?

We're building a real-valued environmental sound classification CNN in Caffe, and a complex counterpart, with appropriate layer functions that pass complex-valued data through the network. We will then run the two head-to-head, and aim to beat the real-valued network with the complex version.

I'd like to give a huge thank you to Stella Yu and Pat Virtue from the International Computer Science Institute (ICSI) for their counsel and advising during this project. You're both amazing researchers and inspiring mentors.




