---
toc: true
layout: post
description: Desc - Movie genre classification using movie posters
categories: [markdown]
title: Multi-label Image Classification
---
This is a tutorial from [Analytics Vidhya](https://www.analyticsvidhya.com/blog/2019/04/build-first-multi-label-image-classification-model-python/#)

For [Setup see here](https://github.com/DexterDSilva/multi-label-img-class/tree/master)
> Note: No attempt has been made to finetune the architecture and reduce the amount of overfitting and hence get a better training/validation loss.

Example Result at the bottom of this page.

The dataset of images contain more than two categories ie it is not a simple either/or 

Each image in the dataset can contain only one category

Example: A dataset containing images such as dog, cat, rabbit, parrot
Each image contains only dog, cat, parrot rabbit

![]({{site.baseurl}}/images/multi-label-img-class.png)

The above is know as multi-label image classification.

Question: Can we predict the genre of a movie by looking at the movie poster? And ofcourse a movie can belong to more than one genre.
![]({{site.baseurl}}/images/multi-label-img-class-2.png)

The key is in the output layer - use a sigmoid activation instead of softmax. With Softmax as the probablity of one increases the probability of the other classses decrease (becuase the sum must equal 1). With Sigmoid however the probabilities are independent of each other. So with sigmoid the architecture will internally create N models where N is the number of classes. Cool huh?!

### Results:
![]({{site.baseurl}}/images/multi-label-op-1.png)
---

![]({{site.baseurl}}/images/aero-robot-with-logo-small.png)![]({{site.baseurl}}/images/onpointai-logo-small.png)
