---
title:  "[미닛타이머] HTML, CSS로 간단한 파이 타이머 구현해보기"
excerpt: "미닛타이머 만들기 1편"
categories: 
- minutetimer
tags:
- HTML
- CSS

toc_label: 타~이~머
toc: true
toc_sticky: true
 
date: 2022-02-16
last_modified_at: 2022-02-16
---


> `CodeSandbox`를 이용하여 제작했습니다. `Codesandbox` 이용법은
👉[온라인 IDE 코드샌드박스](https://eggjini.github.io/html%20/%20css/codesandbox/)를 참고하세요.

타이머 링크: https://eggjini.github.io/minute-timer/

[![image.png](https://i.postimg.cc/Y0CkP8mj/image.png)](https://postimg.cc/62gD2rcN)

우선, 이런 타이머를 HTML과 CSS로 만들어 보도록 합시다!
이 타이머는 제가 직접 HTML과 CSS, 자바스크립트를 이용해서 제작한 사이트예요. 무엇보다 **디자인**에 신경을 좀 썼습니다. *(예쁘면 장땡이지 뭐...)*

# 📌 돌아가는 타이머 구현
저 빙글~빙글 돌아가면서 남은 시간을 **직관적**으로 나타내 주는 타이머를
우선 만들어 봅시다. 

이런 파이타이머를 구현하기 위해서 방법과 소스코드들을 찾아다녔지만
딱히 마음에 들지 않아서 몇 가지만 참고하여 직접 제작했습니다.

> 👉[참고한 소스](https://jsfiddle.net/L5yagfp6/16/)

타이머를 회전시키는 기능은 오로지 `CSS` 로만 구성했습니다.
CSS의 **"키프레임"** 기능을 이용해서요!

## `<HTML>` 소스

~~~html
<div class="timer">
    <div class="mask"></div>
</div>
~~~

## `<CSS>` 소스
~~~css
.timer {
    background: -webkit-linear-gradient(left, skyBlue 50%, #eee 50%);
    /* Foreground color, Background colour */
    border-radius: 100%;
    height: 100px;
    /* Height and width */
    position: relative;
    width: 100px;
    /* Height and width */
    animation-name: time;
    animation-duration: 20s;
    animation-timing-function: linear;
    animation-iteration-count: infinite;
}
.mask {
    border-radius: 100% 0 0 100% / 50% 0 0 50%;
    height: 100%;
    left: 0;
    position: absolute;
    top: 0;
    width: 50%;
   
    animation-name: mask;
    animation-duration: 20s;
    animation-timing-function: linear;
    animation-iteration-count: infinite;
    /* Animation time and number of steps (halved) */
    -webkit-transform-origin: 100% 50%;
}
@-webkit-keyframes time {
    100% {
        -webkit-transform: rotate(360deg);
    }
}
@-webkit-keyframes mask {
    0% {
        background: #eee;
        /* Background colour */
        -webkit-transform: rotate(0deg);
    }
    50% {
        background: #eee;
        /* Background colour */
        -webkit-transform: rotate(-180deg);
    }
    50.01% {
        background: skyBlue;
        /* Foreground colour */
        -webkit-transform: rotate(0deg);
    }
    100% {
        background: skyBlue;
        /* Foreground colour */
        -webkit-transform: rotate(-180deg);
    }
}
~~~
## 👀 소스 설명
`timer` 라는 div 와 `mask` 라는 div이 있습니다.
각각 CSS속성에서 `timer`는 반원을, `mask`도 반원을 만들어 준 거예요.
(하지만 방향이 다르답니다)

`timer`는 시계의 색을 적용해 주고요,`mask`는 배경색으로 적용해 줍니다.
그래서 `timer`라는 반원이 계속 돌고, `mask`는 이리 저리 왔다갔다하며
부분을 가려서 일종의 "눈속임"을 만드는거죠. 

[![image.png](https://i.postimg.cc/rmFw6qB8/image.png)](https://postimg.cc/8F9SMgk3)
이게 `timer` 입니다.

[![image.png](https://i.postimg.cc/R0vMfMVc/image.png)](https://postimg.cc/TKHMvvbw)

그 위를 `mask` 가 덮어요.

[![image.png](https://i.postimg.cc/43wXQrmj/image.png)](https://postimg.cc/CZByFrC4)

배경을 `mask`와 똑같이 해주면, 아무것도 없는것처럼 보이죠?

[![image.png](https://i.postimg.cc/Y9hjGpbd/image.png)](https://postimg.cc/sQC3bRFW)

`mask`는 잠시 안보인다고 치고, `timer`가 이렇게 돌아갑니다.

[![image.png](https://i.postimg.cc/NM3GKRy0/image.png)](https://postimg.cc/XGg6hGkM)

`timer` 위를 `mask`가 덮었기 때문에 이렇게 보입니다.

[![image.png](https://i.postimg.cc/mgLL1Lr7/image.png)](https://postimg.cc/TpsMZXgP)

이렇게 말이죠.
이제 `timer` 가  돌고, 돌고, 돌아서 절반을 넘으면
`mask`를 좌우반전시켜주고 색을 시계 색(빨간색) 으로 바꿔주면 됩니다.

저 위의 그 기---인 코드가 그저 이런 내용이었습니다.

# 📌 타이머 시간 설정
원래 시간은 사용자에게 입력을 받아서 **"자바스크립트"**로 처리해야 하지만,
그건 나중에 하고 우선 아~주 기본적인 기능만 구현해 봅시다.

저 위쪽 CSS 소스에 .timer 와 .mask 클래스가 있는데, 그 각각의 
`animation-duration: [시간(s)]; `
를 수정해 주면 됩니다.

예를 들어서 두 클래스의 애니메이션 시간을
~~~css
.timer.mask {
animation-duration: 60s;
}
~~~
이렇게 설정했다면 타이머는 "1분" 동안 돌아가게 됩니다.

# 📌 마무리
다음 포스팅에서는 "시작" 버튼과 "초기화" 버튼을 만들어 볼 겁니다.
이제 슬슬 타이머의 모습을 갖추게 되겠죠!

> 👉 [전체 소스 코드](https://github.com/Eggjini/minute-timer)
👉 [타이머 써보기](https://eggjini.github.io/minute-timer/)

💛이 포스팅은 ["#타이머 만들기" ](https://eggjini.github.io/categories/#minutetimer)카테고리의 글입니다!
{: .notice--primary} 

