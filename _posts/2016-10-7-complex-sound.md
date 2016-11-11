---
layout: post
title: Complex Sound
date: 2016-10-28 15:01:42
---

This semester I'm writing a paper on complex convolutional neural networks. Here's the big idea:

> ConvNets are amazing. They have practically solved computer vision. However, most machine learning architectures don't train on complex domain data.
>
> What if we could train ConvNets not only on magnitudes of pixel gradients and sounds, but also their relative phases?


1. Why do we want to incorporate phase?

In many types of data (MRI imaging data, musical data, low frequency sound data) there seems to be vital information encoded in the complex domain.

2. What challenges do we face when training CNNs on complex numbers?

Complex numbers are difficult to think about. What does it mean to threshold a complex number? What effect does a gaussian kernel have on backgropagation? How do you convolve pixel gradients or phase? Which activation functions are both meaningful in the complex domain and holomophic?

3. How do we plan on testing?

We're building a real-valued environmental sound classification CNN in Caffe, and a complex counterpart, with appropriate layer functions that pass complex data through the network. We will then run the two head-to-head, and aim to beat the real-valued network with the complex version.

I'd like to give a huge thank you to Stella Yu and Pat Virtue from the International Computer Science Institute (ICSI) for their counsel and advising during this project. You're both amazing researchers and inspiring mentors.
