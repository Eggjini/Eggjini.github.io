---
title:  "그라데이션 CSS 간편하게 적용하기! - WebGradient"
excerpt: "CSS에서 그라데이션, 간편하게 적용해보자"
categories: 
- 꿀팁
tags:
- HTML
- CSS
- 개발자

toc_label: 목차
toc: true
toc_sticky: true
 
date: 2022-02-08
last_modified_at: 2022-02-08
---

- Windows 11
- CodeSandbox / VScode

HTML<sup>[1](#HTML)</sup> 이나 CSS<sup>[2](#CSS)</sup> 를 이용해서 사이트를 제작하고, 디자인하다 보면

[![image.png](https://i.postimg.cc/y6M8m8ys/image.png)](https://postimg.cc/fkvsZZPr)
이런 그라데이션<sup>[3](#gradeition)</sup> 이 어딘가에 필요하곤 하죠.

그럴 때마다 구글 검색을 통해서 그라데이션 불편하게 찾지 말고!
이제 이 사이트 하나로 간편하게 그라데이션 CSS를 적용해 보세요.
- 사이트 바로가기: [https://webgradients.com/](https://webgradients.com/){:target="_blank"}

## 사용 방법
이 사이트를 사용하는 방법은 정말 간단합니다.

우선, 사이트에 접속해서, 원하는 그라데이션 효과를 찾은 다음
바로 CSS코드를 복사 할 수 있어요.

1) 원하는 그라데이션 효과 찾기

[![image.png](https://i.postimg.cc/cCNPJ2fy/image.png)](https://postimg.cc/tZ2BSrr2)
이 사이트에는 무려 180가지의 그라데이션 효과들이 있습니다.
각각 그라데이션들의 색상 코드와 png 파일<sup>[4](#png)</sup> 도 무료로 제공된다고 하네요~

2) CSS (스타일시트) 코드 복사

CSS는 Cascading Style Sheets 의 줄임말로, 마크다운 언어<sup>[5](#MD)</sup> 가
실제로 표시되는 형식이나, 디자인 같은 것들을 표시하는 스타일시트 언어랍니다.
그라데이션의 CSS 코드를 복사하면 여기에 나타나는 그라데이션들을 모드 사용할 수 있어요!

[![image.png](https://i.postimg.cc/8PxMrGj6/image.png)](https://postimg.cc/KRrRdd7G) 

예를 들어, 이러한 그라데이션 효과의 CSS를 사용하고 싶다 하시면
오른쪽 아래 Copy CSS를 클릭하시면 자동으로 클립보드에 복사된답니다.
CSS 코드 뿐만 아니라, 16진수 색상 코드<sup>[6](#color)</sup>도 표기되어서 
포토샵이나 일러스트 같은 프로그램에서도 사용하실 수 있어요.

## 사용  예시
저 산뜻한 그라데이션의 CSS를 복사 해 봤습니다.

`background-image: linear-gradient(to top, #e14fad 0%, #f9d423 100%); `

무슨 뜻인지 알 필요는 없고, *(알아두면 좋긴 합니다만)*
이 CSS를 한번 적용해 보도록 할게요.

[
![image.png](https://i.postimg.cc/nhkBzPQ8/image.png)](https://postimg.cc/RWWNpGRG) 
이렇게 버려둔 HTML 파일을 재탕했습니다...
webgradient 라는 class로 새로운 div 를 만들어 주고, 
연결된 CSS파일에 webgradient라는 클래스에 아까 복사해둔 코드를 넣어봤어요~

[![image.png](https://i.postimg.cc/k5v17s7D/image.png)](https://postimg.cc/5Hjq3wYM)
화려한 그라데이션이 저 작은 글씨<sup>[7](#text)</sup>를 감싸고 있네요...

## 각주 
<a name="HTML">[1]</a>: **HTML**(HyperText Markup Language)은 웹을 이루는 가장 기초적인 구성 요소로,
 웹 콘텐츠의 의미와 구조를 정의할 때 사용합니다.
 
 <a name="CSS">[2]</a>: 캐스케이딩 스타일 시트는 마크업 언어가 실제 표시되는 방법을 기술하는 스타일 언어로, HTML과 XHTML에 주로 쓰인다.
 
<a name="gradeition">[3]</a>: _그라데이션_(Gradation)은 하나의 색채에서 다른 색채로 변하는 단계, 혹은 그러한 기법을 의미하는 단어다.

<a name="png">[4]</a>: 'Portable Network Graphics'의 약자로서 그림 파일 형식 가운데 하나이다.

<a name="MD">[5]</a>: 마크다운은 일반 텍스트 기반의 경량 마크업 언어다. 
일반 텍스트로 서식이 있는 문서를 작성하는 데 사용되어진다.

<a name="color">[6]</a>: 예시) #ffffff (흰색) #ff0000 (빨간색) #000000 (검정색)

<a name="text">[7]</a>: "This is Webgradient!"

## 링크 
오늘 포스팅 관련 코드들은 모두 **깃허브 레포지토리**에 업로드 되어 있습니다.
- 깃허브 바로가기: [https://github.com/Eggjini/Blog-Examples](https://github.com/Eggjini/Blog-Examples){:target="_blank"}

    

