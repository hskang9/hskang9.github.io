---
layout: post
title: 'C++을 파이썬처럼 주피터에서 돌리기'
categories: AI
tags: [cpp, caffe2, jupyter]
---

AI framework 들이 생겨나면서 python api 말고도 c++ api도 제공하고 있지만 c++은 컴파일 언어라 수정할 때마다 컴파일을 해줘야 한다는 점이 불편할 수 밖에 없다.
또한 파일만 컴파일하다 보면 어느 부분에서 잘못됬는지 체크하려 디버깅을 파일을 열거나 돌리면서 해줘야 하는 건 덤;;;

이를 해결하려면 c++을 파이썬처럼 인터프리터 언어처럼 사용되게 하여야 한다.

그래서 나온 게 이 **[cling](https://github.com/vgvassilev/cling)**이다.

이것을 깔면 c++도 주피터 안에서 돌릴 수 있는 것이다.

<!--more-->

{% include advertisements.html %}


cling은 UNIX 운영체제에서 기반한 OS들에게만 지원하니 윈도우를 사용한다면 맥북을 사거나 리눅스를 깔아야 된다.

우선 [여기 클릭](https://root.cern.ch/download/cling/)을 한 뒤 cling에 있는 컴파일된 바이너리 파일 모음들에서 자신의 운영체제에 맞는 바이너리 압축 파일을 가져온다.

압축파일을 풀고 나면 

아래 커맨드를 입력해준다.
```bash
# cling 커널이 돌아가기 위해 먼저 zeromq를 깔아준다.
brew install zeromq # Mac OS X(homebrew)
apt-get install zeromq # Linux
export PATH=<span style="background-color:green">/Users/{username}/</span>/cling/bin:$PATH
cd <span style="background-color:green">/Users/{username}/</span>/cling/share/cling/Jupyter/kernel
pip install -e .
```

cling의 커널 스펙을 쥬피터에게 입력해주기(cling-cpp11, cling-cpp14, cling-cpp17도 가능)

```bash
jupyter-kernelspec install --user cling-cpp17
```

