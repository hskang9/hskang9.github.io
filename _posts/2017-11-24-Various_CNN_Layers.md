---
layout: post
title: '여러가지 합성곱 신경망 레이어들 - InceptionV1(Googlenet)'
featured_image: inception.png
categories: Cocoa/iOS
tags: [Deep Learning, Machine Learning, Keras]
---


## 인셉션이 나오기 전
과학자들은 **ImageNet Large-Scale Visual Recognition Challenge(ILSVRC)** 에서 좋은 성과를 보여주려고 딥러닝에 대해 연구하던 중 여러가지 레이어들이 나왔다.

- **연산도 간단하고 픽셀마다의 피쳐를 계산해서 최대한 정보를 보존시켜준다는 1x1 Convolution(Conv1x1)**
- **연산량을 대폭 줄여주어 cost도 절약되고 overfitting도 줄여주는 MaxPooling**
- **이외 여러가지 커널 사이즈들의 Convolution layer들(3x3, 5x5)**


물론 각 레이어마다 신경망의 정확도를 높이는 데 기여를 하기는 했지만 어느 쪽이 좀 더 효과적인지는 전혀 몰랐는데...

![whattochoose](posts/whattochoose.png)
## Reference
- [Going Deeper with Convolutions](https://arxiv.org/abs/1409.4842)
- [Udacity](www.udacity.com)

{% include advertisements.html %}
