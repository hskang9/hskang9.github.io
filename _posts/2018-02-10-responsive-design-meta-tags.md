---
layout: post
title: 'Responsive design에 짚고 넘어가야만 하는 <meta> tag들'
featured_image: inception.png
categories: front_end
tags: [front_end, web_development]
---

# 1. Viewport

## Viewport란?

viewport란 사용하는 디바이스에서 웹앱이 사용할 수 있는 범위를 지정해주는 <meta> 태그입니다.
이 <meta> 태그를 사용하면 다음 사항을 기기마다 css로 일일이 크기를 정해주지 않고도 웹 앱의 컨텐츠가 디바이스 스크린 양 옆으로 빠져나가는 것을 예방해줄 수 있습니다.

{% include image_caption.html imageurl="/images/posts/contents_out.png" title="contents_out" caption="이런 거" %}


```html
   <head>
     <meta name="viewport" content="width=device-width, initial-scale=1">
   </head>
```

위처럼 <meta>태그를 웹 앱의 <head>태그 안에 쓰는데 아래로 스크롤하며 내려가는 웹 앱의 경우 width만 맞춥니다. 이외 WebVR이나 게임 같은 경우는 height를 사용하는 경우도 존재합니다.


# 2. 
