---
layout: post
title: 맥OSX에 maven 설치하기
category: etc
comments: true
tags: [maven]
---

맥에 메이븐 설치를 위해 검색을 하고 블로그에 나와있는 방법으로 설치 진행.

아파치에서 메이븐을 다운받아 /usr/local 에 압축을 푼 후..

.bash_profile 에 path를 추가했다.

그리고 source .bash_profile 하니 성공.

헌데 새 창을 띄우거나 리부트하여 다시 명령어를 입력하니 mvn커맨드를 못찾는단다..

일단 이유는 찾지못했고.. 나와 같은 고민을 올린 스택오버플로우 글을 여러개 보았지만 해결은 되지 않았다.

구글링하여 homebrew로 설치하는 방법을 알아냄.

~~~C
$ brew install maven
~~~

나는 이미 homebrew 를 설치해놓았기에 손쉽게 install 가능.

[brew.sh](https://brew.sh) 여기도 참고해보자.

