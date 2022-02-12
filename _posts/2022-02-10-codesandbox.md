---
title:  "요즘 인기있는 온라인 코드 작성기 (IDE) 코드샌드박스! CodeSandbox"
excerpt: "코드샌드박스로 간단한 웹페이지를 만들어 봅시다."
categories: 
- html_css
tags:
- HTML
- 자바스크립트

toc_label: 코드샌드박스
toc: true
toc_sticky: true
 
date: 2022-02-10
last_modified_at: 2022-02-10
---

- windows 11
- [CodeSandbox](https://codesandbox.io){: target="_blank"}

HTML 과 CSS를 작성하고, JS를 연결해 웹사이트를 만들기 위해서 VScode 라는 IDE를 사용하곤 했습니다. 하지만 간단한 수정 사항이 있음에도 프로그램을 실행시켜야 하고, 수정 결과를 보기에도 시간이 꽤 오래 걸렸답니다. *(그냥 귀찮아서...)*

그래서 오늘 바로 CodeSandbox라는 무려 **온라인** 코드 작성기를 소개시켜 드리려고 합니다.
HTML, CSS는 물론 자바스크립트나 Vue, React 같은 다양한 종류도 있더라고요~

## 회원가입, 로그인
👉 [사이트 바로가기](https://codesandbox.io){: target="_blank"}

[![image.png](https://i.postimg.cc/rmbM9zNT/image.png)](https://postimg.cc/2b4skkt9)

코드샌드박스 사이트에 접속하면 이런 화면이 뜰 텐데요,

[![image.png](https://i.postimg.cc/QC1C9pGw/image.png)](https://postimg.cc/dZQwgZ0j)

따로 회원가입 없이 기존 **깃허브** 계정이나 **구글** 계정으로 로그인할 수 있습니다.
이건 편리성이나, 보안성 측면으로 좋은 것 같네요.
저는 제 기존 깃허브 계정을 이용해서 로그인을 했습니다!

## 템플릿 이용하기

[![image.png](https://i.postimg.cc/3wqxtL3z/image.png)](https://postimg.cc/v1WyBtgv)

`Create Sandbox`라는 버튼을 누르니 이렇게 다양한 템플릿들을 볼 수 있습니다.
아마 **Static**이 **HTML **파일을 의미하는 것 같고요, Vue, Js, Reack, Node.js 등 정말 다양한 기능들을 볼 수 있습니다.

이번에는 **HTML**을 이용해서 간단한 웹페이지를 만들기 위해 **Static** 이라는 템플릿을 눌러서 새로운 **샌드박스**를 만들어 주도록 할게요.

[![image.png](https://i.postimg.cc/Z5TFrLYr/image.png)](https://postimg.cc/6ymvKnv3)

그러면 이렇게 **HTML**에서 기본적인 `<head>`나 `<body>`같은 코드들이 템플릿으로 미리 작성되어 있고요, 헤드 태그 안에 반응형 웹을 위한 `<meta>`태그도 있습니다.
*대박 편하네요*

## 사이트 만들어보기
그러면 **CodeSandbox**를 이용해서 간단한 사이트를 하나 만들어 보도록 할게요.
음... 간단하게 설명도 해 드리도록 하겠습니다. *(이건 HTML 강좌인가...?)*

### 사이트 개요
우선 어떤 사이트를 만들지 정해 보도록 할게요. **HTML** 과 **CSS**, **JS**를 모두 이용해서 사이트를 만드려면 바로 **버튼**만한게 없죠. **HTML**로 버튼을 만들고, **CSS**로 버튼을 꾸미고, **자바스크립트**로 버튼을 눌렀을 때 알림창 (alert)를 띄워 보도록 하겠습니다.
*(참고로 자바스크립트와 Js는 같은 말입니다)*

### HTML 작성
이 사이트에서 가장 중요한 **버튼**을 만드는 코드를 우선 알려 드릴게요.
**HTML**에서는 `<body>`태그 안에 작성된 내용이 사이트에 보여지게 되는데요, 
**HTML**은 이렇게 꺽쇠 `<` 로 태그를 작성합니다.

`<태그>`의 형태로 태그를 열면, `</태그>`의 형태로 그 태그를 다시 닫아 줘야 합니다.
이 태그 사이에 들어간 내용이 표시가 되는 거예요.

버튼을 만들어 주는 태그는 바로 `<button>`이예요.
~~~ html
<button  class="alertBtn">클릭!</button>
~~~
이렇게 하면, class가 **alertBtn**이고, 클릭! 이라는 글자가 쓰여 있는 버튼이 만들어진답니다.
여기서 class는 쉽게 이 요소의 이름을 정해 주는 것과 비슷해요. class와 비슷한 속성으로 id가 있는데, id는 유일한 요소에 사용됩니다.

class와 id 모두 다 CSS나 Js에서 이 요소에 대한 값들을 설정하기 위해서 사용해요.

CodeSandbox에서 `Ctrl + S`를 누르면 작성한 내용이 저장됩니다.
저장된 후 바로 오른쪽 Preview 페이지에 표시가 돼요.

[![image.png](https://i.postimg.cc/fRmyR4QC/image.png)](https://postimg.cc/0z5PVBQK)

이제 이 버튼을 꾸며 봅시다!

### CSS 작성하기

자! CSS는 하나하나 작성하기엔 너무 비효율적이니 **템플릿**을 가져와보도록 할게요.
구글에 검색을 해 보면 **잘~** 정리된 버튼 CSS 모음집을 볼 수 있습니다.

[![image.png](https://i.postimg.cc/g2GZ6kcj/image.png)](https://postimg.cc/3dbRshvQ)

코드샌드박스 왼쪽에서 New File 을 눌러서, 
`style.css`라는 파일을 만들어 보도록 하겠습니다.


~~~ CSS
.alertBtn {

/*중앙 정렬 코드*/
left:  50%;
top:  50%;

margin-left:  -100px;
margin-top:  -25px;

width:  200px;
height:  50px;
/*중앙 정렬 코드 끝*/

position:  absolute;
border:  none;
display:  inline-block;
padding:  15px  30px;
border-radius:  15px;
font-family:  "paybooc-Light", sans-serif;
box-shadow:  0  5px  10px  rgba(0, 0, 0, 0.2);
text-decoration:  none;
font-weight:  600;
transition:  0.25s;
background-color:  #408080;
color:  #ffeee4;
cursor:  pointer;
}

.alertBtn:hover {
transform:  scale(1.1);
}
~~~

[![image.png](https://i.postimg.cc/FKgK0wpZ/image.png)](https://postimg.cc/Ty1G67ZL)

버튼이 훨씬 보기 깔끔해졌습니다.

중앙 정렬을 위해서 화면의 50%, 50% 위치로 이동시키고
요소 크기의 반틈만큼 다시 이동시켰습니다.

뭐 CSS는 중요한 부분은 아니니 이렇게 코드를 공개해 드리고 넘어가겠습니다.
CSS의 자세한 내용에 대해서는 다른 포스팅에서 다룰 에정입니다.

### 자바스크립트 작성
버튼을 눌렀을 때 어떤 동작을 할 것인지 자바스크립트로 쉽게 작성이 가능합니다.
자바스크립트의 기본적인 문법을 잘 알고 계시면, 
**HTML** 과 연결시키는 것도 아주 쉽게 할 수 있습니다. 

자바스크립트를 작성하기에 앞서, **HTMl** 파일에 자바스크립트를 연결하는 방식은 크게 2가지가 있습니다. **HTML** 안에 스크립트를 집어넣는 **인라인** 방식과, 자바스크립트 파일을 따로 만들어서 연결시키는 방식이 있어요.

자바스크립트의 양이나 **HTML**의 양이 꽤 많다면, 무조건 따로 파일을 만들어서 연결하는 것을 추천드리지만, 이번만큼은 정말 간단한 이벤트 리스너 코드만 작성할 것이기 때문에 **HTML** 코드 안에 스크립트를 집어 넣는 **인라인** 방식을 이용하도록 하겠습니다.

[![image.png](https://i.postimg.cc/VkzsmKm0/image.png)](https://postimg.cc/KRsh5rKm)

이렇게 **HTML**에서 `<body>` 태그가 끝나기 바로 위에, `<script>` 태그를 작성해 주세요.

~~~ html
<script>

document.querySelector(".alertBtn").addEventListener("click", alert("Wow, it's Button!"));

</script>
~~~
이렇게 스크립트를 작성해 주면, 버튼을 클릭했을 때 **"Wow, it's Button!"** 이라고 알림창이 뜨게 됩니다.



