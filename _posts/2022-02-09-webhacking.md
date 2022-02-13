---
title:  "웹 해킹 연습 사이트 - webhacking.kr 사용법"
excerpt: "webhacking.kr 1번, 14번, 16번 문제 해설!"
categories: 
- 보안 / 해킹
tags:
- 웹해킹
- 자바스크립트

toc_label: 목차
toc: true
toc_sticky: true
 
date: 2022-02-09
last_modified_at: 2022-02-09
---

- windows 11
- [webhacking.kr](https://webhacking.kr){: target="_blank"}

사이트를 제작하면서 보안에도 신경을 써야 한다는 생각이 들었습니다.
이곳 저곳 찾아보니 보안에 대해서도 어느 정도 알면 좋지 않을까 해서

[![image.png](https://i.postimg.cc/13BjGHVw/image.png)](https://postimg.cc/VJSg1XRk)

직접 웹 해킹을 해보면서 알아가 보도록 합시다. (물론 합법으로요...)

## 웹 해킹 연습 사이트
웹 해킹의 다양한 방식적인 부분을 게임(?) 같이 한번씩 해 볼 수 있는 사이트입니다.
워낙 웹 해킹 사이트 중에서도 유명한 사이트라서 한번쯤은 접해 봤을지도 모르겠네요.

<https://webhacking.kr>{: target="_blank"}

사이트 주소마저 웹해킹입니다.

### 회원가입
사이트에 접속해서 왼쪽에 Login / Join 버튼을 눌러서 계정을 생성해 주세요.
계정이 있어야 진행이 될 듯 합니다.

[![image.png](https://i.postimg.cc/jdKcMfbX/image.png)](https://postimg.cc/5j7806jY)

간단하게 ID와 비밀번호, 이메일을 적어 주면 바로 계정이 생성이 됩니다.
바로 위에서 로그인을 해 주면, 로그인에 성공했다고 메세지가 뜰 거예요.

### 문제 풀어보기
Challenge(old) 라는 메뉴에 들어가면, 간단한 해킹 연습 문제들이 나오게 됩니다.

[![image.png](https://i.postimg.cc/kXX8VvCk/image.png)](https://postimg.cc/w3Z3ZJ7V)

저는 이미 몇 개 풀어 보아서, 완료된 항목은 이렇게 하늘색으로 표시가 되네요.
옆에 아이콘으로 어떤 방식의 문제인지도 알려줍니다. 

[![image.png](https://i.postimg.cc/X7JGNNcW/image.png)](https://postimg.cc/t7KC2jMv)

문제를 클릭하면 이렇게 각 문제마다 다른 페이지가 나옵니다. 
어떻게 해야 할지 잘 알 수 있는 문제들도 있지만, 
대게는 뭘 해야할지 모르는.... 그런 문제들도 꽤 많습니다.

## 문제 풀이
우선 제가 풀어 본 몇 가지 문제들을 풀이를 해 드리도록 하겠습니다.
우선 웹 해킹에 대해 공부하기 전에, php나 Js 같은 웹 구성 언어들의 기본적인 문법 등은 알고 있으면 도움이 됩니다.

저는 이미 풀어봐서 처음 모습과 좀 다르게 표시되는 것 때문에, 
다른 계정을 만들어서 진행하였습니다.

### 1번 문제 (php, 쿠키)

1번 문제를 클릭하면, level 의 값과, view source라는 링크가 나오게 됩니다.
우선 view source를 클릭해 보세요. (우클릭으로 새 창에서 열어보세요)

~~~ php
<?php  
if(!is_numeric($_COOKIE['user_lv'])) $_COOKIE['user_lv']=1;  
if($_COOKIE['user_lv']>=4) $_COOKIE['user_lv']=1;  
if($_COOKIE['user_lv']>3) solve(1);  
echo "<br>level : {$_COOKIE['user_lv']}";  
?>
~~~

이렇게 php 구문만 따로 해석해 보겠습니다.

**'user_lv'** 이라는 쿠키가 숫자가 아니면, 쿠키의 값을 1로 정해줍니다.
그리고 쿠키의 값이 4 이상이면, 또 쿠키의 값을 1로 정합니다.
또 쿠키의 값이 3 초과면 1번 문제를 **solve** 했다고 구문이 나와 있습니다.

그렇다면 이 문제는 **"쿠키"** 를 조작하는 문제라고 볼 수 있겠네요.
[Chrome Webstore](https://chrome.google.com/webstore/){: target="_blank"} 에서 **"EditThisCookie"** 라는 확장앱을 설치해 줍니다.

- [설치 바로가기](https://chrome.google.com/webstore/detail/editthiscookie/fngmhnnpilhplaeedifhccceomclgfbg?hl=ko){: target="_blank"}

[![image.png](https://i.postimg.cc/bwLqZ1zF/image.png)](https://postimg.cc/hXJkwzQ9)

이렇게 확장 프로그램을 실행하면, 쿠키의 이름과 값이 나오게 되죠.
아까 php 구문에서 쿠키의 값이 3이 초과될 경우 성공이라고 했습니다.
그런데 그 구문 앞에 먼저 4 이상이면 1로 다시 세팅한다는 구문이 있어요.
성공하려면, 쿠키의 값이 3 초과 4 미만이여야 한다는 겁니다.
`3 < user_lv <4`

그러면 3.5로 쿠키를 설정해 봅시다.

[![image.png](https://i.postimg.cc/CKXT8N9J/image.png)](https://postimg.cc/DWrMkqvb)

뭐 이미 풀었다고 뜨긴 하지만... 성공입니다.

### 14번 문제 (Js)

14번 문제는 자바스크립트에 관한 문제인 것 같네요. 이 중에서 제가 그나마 잘 알고 있는 것이 자바스크립트니까 한번 풀어 보겠습니다.

페이지를 열면, 그냥 값을 입력하는 폼만 있고 아무것도 없네요. 
개발자 도구 [F12] 를 눌러서 소스를 한번 보도록 합시다.

[![image.png](https://i.postimg.cc/K8WspYQ8/image.png)](https://postimg.cc/WdMnhTQB)

`<script>` 부분을 펼쳐 보면, 

~~~ javascript
function ck(){ 
var ul=document.URL; 
ul=ul.indexOf(".kr"); 
ul=ul*30; 

if(ul==pw.input_pwd.value) { 
location.href="?"+ul*pw.input_pwd.value; 
} else { 
alert("Wrong"); } 
}
~~~
이렇게 ck라는 함수 (function) 가 있네요.
form 소스를 보니, check 라는 버튼을 클릭하면 이 ck 함수를 실행하게 되어 있습니다.

ck 함수는 변수 ul의 값을 이 사이트의 URL로 정하고, 
이 ul 값에서 ".kr" 이 있는 글자가 몇번째인지를 다시 이 값으로 정하고
마지막으로 이 값에 30을 곱해줍니다. 그래서 최종 결과값이 ul 이 되겠죠.

조건문에서는 ul의 값이 pw.input_pwd.value, 
그러니까 아까 글자 입력하는 칸에 입력한 값이랑 같으면 됩니다.

쉽게 이야기해서, ul의 값을 알아내서 그 칸에 입력하면 된다는거죠.
알아내 봅시다.

아까 개발자 모드 [F12] 에서 두 번째 탭에 보면 **"콘솔"** 이라는 탭이 있습니다.
여기서 간단한 Js 구문을 실행할 수 있죠. 우선 이 코드를 입력해 봅시다.

~~~ javascript
alert(document.URL);
~~~
여기서 alert는 괄호 안의 값을 알림창으로 출력한다는 내용입니다.

[![image.png](https://i.postimg.cc/sxBMcw2X/image.png)](https://postimg.cc/V08ss9nQ)

이게 첫번째 ul의 값입니다.
이제 이 코드를 입력해 볼까요?

~~~ javascript
alert("https://webhacking.kr/challenge/js-1/".indexOf(".kr");
~~~

이번에는 document.URL에서 .kr이 몇 번째 글자인지를 알려줍니다.

[![image.png](https://i.postimg.cc/PxvLbSJq/image.png)](https://postimg.cc/k69XqFxr)

18번째라고 하네요.
그러면 여기에 30을 곱해 볼까요? 계산기를 써도 되지만, 자바스크립트로 계산을 할 수도 있답니다.

[![image.png](https://i.postimg.cc/gjDG3hVJ/image.png)](https://postimg.cc/tns0jYmQ)

그러면, 540을 입력하고 "check" 버튼을 눌러 봅시다.

[![image.png](https://i.postimg.cc/15v9tpR7/image.png)](https://postimg.cc/GHs0gTyv)

성공입니다.

### 16번 (Js)
자바스크립트 문제가 나름 쉬운지라, 마지막으로 Js 문제만 하나 더 풀어 봅시다.

[![image.png](https://i.postimg.cc/QtgDr7nb/image.png)](https://postimg.cc/k65zQ2C6)

이렇게 깜깜한 화면에 노란색 **별** 하나가 있네요.
마찬가지로 개발자 도구 [F12]를 눌러서 스크립트 부분만 확인해 봅시다.

~~~ javascript
document.body.innerHTML+="<font color=yellow id=aa style=position:relative;left:0;top:0>*</font>"; 

function mv(cd){ 
kk(star.style.left-50,star.style.top-50); 

if(cd==100) star.style.left=parseInt(star.style.left+0,10)+50+"px"; 
if(cd==97) star.style.left=parseInt(star.style.left+0,10)-50+"px"; 
if(cd==119) star.style.top=parseInt(star.style.top+0,10)-50+"px"; 
if(cd==115) star.style.top=parseInt(star.style.top+0,10)+50+"px"; 
if(cd==124) location.href=String.fromCharCode(cd)+".php"; // do it! } 

function kk(x,y){ rndc=Math.floor(Math.random()*9000000); 

document.body.innerHTML+="<font color=#"+rndc+" id=aa style=position:relative;left:"+x+";top:"+y+" onmouseover=this.innerHTML=''>*</font>"; }
~~~
html 코드도 보면
~~~ html
<body bgcolor="black" onload="kk(1,1)" onkeypress="mv(event.keyCode)">
~~~
keypress, 그러니까 키보드를 클릭하는 이벤트가 발생하면 mv 함수를 실행하네요.
그리고 자바스크립트에 cd의 값이 124일때 주석에 //do it! 이라고 되어 있네요.
그러면 onkeypress 이벤트를 그냥 cd = 124로 수정해 보도록 합시다.

~~~ html
<body bgcolor="black" onload="kk(1,1)" onkeypress="mv(event.cd=124)">
~~~

그러고 키보드의 아무 키나 눌러보면,
[![image.png](https://i.postimg.cc/vmQLzwwZ/image.png)](https://postimg.cc/rDPrVbpB)

바로 풀리네요.

사실 이 문제는 원래 이렇게 푸는 문제가 아닙니다.
별의 위치나 그런 것들을 조합해서 알아내야 하지만, 이렇게 바로 푸는 방법도 있습니다.

## 마무리
이런 문제들을 처음 접해보긴 했지만 풀어 보니 재미있긴 하네요.
여러분들도 사이트에 들어가서 한 번 풀어 보시면 좋을 듯 합니다.
앞으로 보안 관련 글들도 종종 올릴 테니 많이 찾아주세요!

## 링크
- [연습 사이트](webhacking.kr){: target="_blank"}
- [PHP](http://www.tcpschool.com/php/php_intro_intro){: target="_blank"}
- [쿠키 조작 확장앱]((https://chrome.google.com/webstore/detail/editthiscookie/fngmhnnpilhplaeedifhccceomclgfbg?hl=ko)){: target="_blank"}
