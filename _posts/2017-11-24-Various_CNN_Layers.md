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


물론 각 레이어마다 신경망의 정확도를 높이는 데 기여를 하기는 했지만 어느 쪽이 좀 더 효과적인지에 대해 고민하고 있었는데...

{% include image_caption.html imageurl="/images/posts/whattochoose.png" title="whattochoose" caption="모두 도움이 되긴 하지만 고르라고 하니 고민된다." %}

구글의 연구자들은 고민을 하다가 Min Lin의 논문인 [Network in Network](https://arxiv.org/abs/1312.4400)를 읽게 되고 2010년에 개봉한 영화인 인셉션 meme "we need to go deeper"를 떠올리며 그냥 레이어들을 합쳐버리기로 결심한다.<strike>네...?</strike>

>“codenamed Inception, which derives its name from the Network in network paper by Lin et al [12](https://scholar.google.com/citations?user=BGONmkIAAAAJ&hl=en)
in conjunction with the famous “we need to go deeper” internet meme [1](http://knowyourmeme.com/memes/we-need-to-go-deeper)” <cite>― Inventors of inception module</cite>

{% include image_caption.html imageurl="/images/posts/whattochoose.png" title="weneedtogodeeper" caption="문제의 그 짤" %}

## 구조 

## 결론
- padding에서 'same'옵션은 서로 다른 케이스의 레이어들을 합칠 때 쓰인다.
- 짤은 21세기의 명화다. 짤을 감상하며 영감을 얻도록 하자.


## Reference
- [Going Deeper with Convolutions](https://arxiv.org/abs/1409.4842)
- [Udacity](www.udacity.com)

{% include advertisements.html %}

## 다음 편 예고
이렇듯 뭐든지 합쳐서 넣어버리는 <strike>연산량 노답</strike> 인셉션 레이어에 의해 처리해야 할 패러미터는 기하급수적으로 늘어나게 되고 연산량이 많아지면서 전 구글 엔지니어이자 케라스 창시자인 Francois Chollet은 좀 더 효율적인 컨볼루션 신경망에 대해 고려하게 되는데...
여러가지 합성곱 신경망 레이어들 - Xception

## 앞으로 연재 
