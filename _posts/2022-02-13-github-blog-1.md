---
title:  "[깃허브 블로그]깃허브 블로그 만들고 설정하기, Minimal Mistakes"
excerpt: "Minimal Mistakes 테마로 깃허브 블로그를 만들고, 기본 설정도 해 보자!"
categories: 
- 깃허브 블로그
tags:
- Minimal Mistakes
- 깃허브

toc_label: 목차
toc: true
toc_sticky: true
 
date: 2022-02-13
last_modified_at: 2022-02-13
---

💜 이 포스팅은 깃허브 블로그에 대한 포스팅이예요.
다른 포스팅을 보고 싶다면 [👉깃허브 카테고리](https://eggjini.github.io/categories/#github)를 참고하세요!
{: .notice--primary} 

제 블로그는 바로 **깃허브**로 만들었답니다. 깃허브는 코드를 업로드해 공유할 수 있는 다양한 기능들을 가지고 있지만, 이렇게 홈페이지를 호스팅 할 수 있는 기능도 가지고 있어요!
깃허브로 간단하게 블로그를 만드는 방법을 알려 드릴게요.👻

# 📌레포지토리 만들기
깃허브에서 **특정한 이름**으로 레포지토리를 만들어 주기만 하면,
자동으로 깃허브 페이지에 호스팅된답니다.

그 레포지토리에 블로그나 홈페이지를 구성하는 파일들을 업로드 해 주면
자동으로 그 파일들을 이용해 블로그나 홈페이지가 만들어져요!

## 1️⃣ 스킨 포크해 오기
이 깃허브 블로그를 더 쉽게 만들기 위해서, 이미 기본적인 틀을 갖추고 있는 다양한 스킨들이 있답니다. 이 **스킨**을 이용해서 깃허브 블로그를 만들면 아주 쉽게 만들 수 있어요.

제가 추천하는 스킨은 바로 "Minimal Mistakes"라는 스킨입니다. 
디자인도 간단하고, 폴더 구조도 쉬운 편이라 수정하고, 커스터마이징하기 수월합니다.

- 👉 [스킨 링크](https://github.com/mmistakes/minimal-mistakes)

위 링크에 접속하면 깃허브 레포지토리가 하나 보일 겁니다.
위쪽에 **Fork** 버튼을 눌러 포크해 주세요.

[![image.png](https://i.postimg.cc/QdTcbczq/image.png)](https://postimg.cc/68B764t7)

## 2️⃣레포지토리 이름 변경
포크해 온 레포지토리에서 `Settings` 탭에 들어가서, 레포지토리 이름을
> `깃허브 닉네임`.github.io

로 변경해 주세요.

[![image.png](https://i.postimg.cc/T2sy4pgN/image.png)](https://postimg.cc/4nzNK48p)

그러면, https://깃허브 닉네임.github.io 라는 링크로 여러분의 깃허브 블로그가 만들어졌을 겁니다. 아직은 아무 설정도 하지 않은 상태이기 때문에, 기본으로 설정된 블로그가 보여질 거예요.

# 📌블로그 설정하기 
이제, 여러분의 블로그를 설정해 주어야 합니다. 기본 정보들부터 해서 다양한 설정들이 있으니 여러분 마음대로 설정할 수 있어요.

## 1️⃣ _config.yml
블로그에 대한 기본적인 정보들을 담고 있는 파일이예요.
별다른 폴더 안에 들어있지 않고, 바로 찾아볼 수 있답니다.

[![image.png](https://i.postimg.cc/jqfWBRcs/image.png)](https://postimg.cc/0r82wRh3)

```yml
minimal_mistakes_skin    : "custom" 

# Site Settings
locale                   : "ko-KR"
title                    : "에그지니 Blog"
title_separator          : "-"
subtitle                 : # site tagline that appears below site title in masthead
name                     : "에그지니"
description              : "디자이너 + 개발자 + 해커"
url                      : "https://eggjini.github.io"
baseurl                  : # the subpath of your site, e.g. "/blog"
repository               : "https://github.com/Eggjini/eggjini.github.io" 
teaser                   : # path of fallback teaser image, e.g. "/assets/images/500x300.png"
logo                     : # path of logo image to display in the masthead, e.g. "/assets/images/88x88.png"
masthead_title           : # overrides the website title displayed in the masthead, use " " for no title
# breadcrumbs            : false # true, false (default)
words_per_minute         : 200
```
- minimal_mistakes_skin: 블로그 스킨을 지정하는 옵션이랍니다. 
  - `air` `contrast` `dark` `dirt` `mint` `sunrise` `aqua` `neon` `plum` 이 
  기본적으로 포함되어 있어요.
  - 저는 커스텀 스킨을 사용하는데, 스킨을 제작하는 방법은 다음 포스팅에서 알려드릴게요.
- locale: 국가와 언어를 설정하는 옵션이예요.
  - 한국 / 한국어는 ko-KR, 미국 / 영어는 en-US 랍니다.
- title: 블로그의 이름을 설정하는 옵션이예요.
- description: 블로그 설명을 설정한답니다. 검색 결과에서 주로 노출돼요.
- url: 블로그 링크를 입력하면 됩니다. 
- repository: 블로그 레포지토리 링크를 입력하면 됩니다.
  - url과 repository 링크가 잘못 입력되면 오류가 발생할 수 있어요.
- words_per_minute는 1분에 읽는 글자수를 설정하는 옵션이예요. 블로그에 표시되는 "포스팅을 다 읽는데 소요되는 예상 시간"을 이 값을 통해 지정된답니다.

~~~yml
# Site Author
author:
  name             : "에그지니"
  avatar           : "/assets/egg.png" 
  bio              : "ver 2.0"
  location         : "대한민국"
  email            : "egg.design@daum.net"
  links:
    - label: "Tistory"
      icon: "fas fa-fw fa-link"
      url: "https://eggdesign.tistory.com"
    - label: "Velog"
      icon: "fas fa-fw fa-link"
      url: "https://velog.io/@egg_jini"
    - label: "GitHub"
      icon: "fab fa-fw fa-github"
      url: "https://github.com/Eggjini"

# Site Footer
footer:
  links:
    - label: "Email"
      icon: "fas fa-fw fa-envelope-square"
      url: "mailto:egg.design@daum.net"
    - label: "GitHub"
      icon: "fab fa-fw fa-github"
      url: "https://github.com/Eggjini"

~~~
 - site author: 블로그 작성자의 정보를 입력해요.
     - name: 이름을 설정합니다. 저 같은 경우에는 "에그지니"로 설정했어요.
     - avarta: 프로필 사진을 설정합니다. assets 폴더에 이미지를 업로드하고, 그 위치를 적어 주면 됩니다. 자세한 내용은 아래에 적어 놓을게요~
     - bio: 카톡으로 치면 "상태메세지" 같은 개념. 자기소개를 짧게 적어 주면 됩니다.
     - location: 위치는 본인의 위치나, 원하는 내용을 적어 주셔도 됩니다.
     - email: 여러분의 이메일을 적어 주면, 자동으로 이메일을 보낼 수 있는 링크가 생성돼요 (짱 신기!!) 
     - links: 여러분의 SNS 링크들을 적어 주면 됩니다. 안쓰는 SNS는 지워버리세요!
- site footer: 블로그 맨~ 아래에 있는 푸터에 들어갈 내용이예요.
   - 사용하는 SNS 링크만 적어 주고, 나머지는 지워버리세요!

## 2️⃣ 프로필 사진
프로필 사진은 `assets` 폴더에 업로드 한 뒤, 아까 수정했던 `_config.yml` 에 `avatar` 속성을 `/assets/파일이름` 형태로 지정해 주면 됩니다.

[![image.png](https://i.postimg.cc/hjyHrFJ6/image.png)](https://postimg.cc/R6tsSDLL)

저는 이렇게 `egg.png` 라는 프로필 사진을 업로드 해 줬으니 `_config.yml` 의 `avatar` 속성을 `/assets/egg.png` 로 설정해 주었어요.

## 3️⃣ navigation.yml

> 📂 파일 위치: _data / navigation.yml

[![image.png](https://i.postimg.cc/BnCsKVg9/image.png)](https://postimg.cc/0zrLgZFc)

블로그 맨 위에 있는 이러한 메뉴들을 설정하는 파일이예요.

~~~yml
main:
	- title: "카테고리"
	url: https://eggjini.github.io/categories/
	- title: "태그"
	url: https://eggjini.github.io/tags/
	- title: "TISTORY"
	url: https://eggdesign.tistory.com
	- title: "VELOG"
	url: https://velog.io/@egg_jini
~~~

`title` 에 표시될 이름을 작성해 주고, `url` 에 클릭하면 이동할 위치를 적어 주면 됩니다.
여러분의 다른 사이트에 연결해도 좋고, 블로그 내의 `카테고리` 나 `태그` 에 연결해 주어도 좋아요. 

카테고리나 태그 페이지를 만드는 방법은 다른 포스팅에서 자세하게 알려 드릴게요~

## 4️⃣ 본문 폭 조정하기

> 📂 파일 위치: _sass / minimal_mistakes / _variables.scss

**Minimal Mistakes** 블로그에는 사이드바가 있고, 오른쪽에는 목차가 나와 있습니다.

[![image.png](https://i.postimg.cc/KvHty0Lb/image.png)](https://postimg.cc/568XBqnK)

이렇게 사이드바와 목차가 나와 있는데, 이 폭들을 수정해 볼 거예요.

`_variables.scss` 파일을 쭈-욱 아래쪽으로 스크롤을 내려 보면,

~~~scss
/*
Grid
========================================================================== */

$right-sidebar-width-narrow: 100px !default; // default 200px

$right-sidebar-width: 200px !default; // default 300px

$right-sidebar-width-wide: 250px !default; // default 400px
~~~

이러한 코드들을 볼 수 있습니다. 적절한 크기에는 정답이 없으니 여러분들 입맛대로 바꿔서 사용하세요~

## 5️⃣ 링크 밑줄 없애기

블로그 기본 설정으로는, 링크에 <u>이런 밑줄</u>이 있어서 은근히 거슬립니다.
사실 밑줄은 적당히 있으면 강조 효과도 있고 좋지만, 링크마다 밑줄이 붙어있으니...
링크의 밑줄을 없애 보도록 할게요. *(아! 물론 선택사항입니다)*

> 📂 파일 위치: _sass / minimal-mistakes / _base.scss

~~~scss
/* links */

a {
	&:focus {
	@extend %tab-focus;
	}

	&:visited {
	color: $link-color-visited;
	}
	
	&:hover {
	color: $link-color-hover;
	outline: 0;
	}
}
~~~
`Ctrl + F` 를 눌러 **links** 라고 검색을 해 주면, 이런 속성들이 나옵니다.
이 속성들은 여러분 블로그의 "모든 링크"에 적용이 되는 속성들이예요.

a 바로 아래줄에 
```scss
	text-decoration-line: none;
```
이 코드를 적용해 주면 됩니다.

**<최종 완성 코드>**
~~~scss
/* links */

a {
	text-decoration-line: none;

	&:focus {
		@extend %tab-focus;
	}

	&:visited {
		color: $link-color-visited;
	}

	&:hover {
		color: $link-color-hover;
		outline: 0;
	}

}
~~~

## 6️⃣ 글자 크기 바꾸기

> 📂 파일 위치: _sass / minimal-mistakes / _reset.scss

제 블로그는 코딩이나 프로그래밍에 관련된 포스팅들을 다루고 있어서 비교적 **큰 글자**를 사용하고 있어요. 아무래도 큰 글자가 보기에도 편하고, 시원시원한 느낌이더라고요.

~~~scss
@include breakpoint($medium) {
    font-size: 17.3px;
  }

  @include breakpoint($large) {
    font-size: 17.3px;
  }

  @include breakpoint($x-large) {
    font-size: 17.3px;
  }
~~~

위에 있는 코드라 쉽게 찾을 수 있을 겁니다. 

[![image.png](https://i.postimg.cc/Hx1k0yyF/image.png)](https://postimg.cc/VS4wm54F)

여기서 font-size 값을 바꿔 주면, 글자 크기가 바뀐답니다.
너무 작으면 모바일에서 포스팅을 볼 때, 글씨를 알아볼 수 없을수도 있다고 하니
적당히 조절하는 것을 추천드려요.

# 📌포스팅 작성하기
블로그의 기본적인 설정들을 마쳤으니 이제 포스팅을 써 볼 차례입니다.
깃허브 블로그의 포스팅은 기본적으로 `markdown` 형식으로 작성합니다. 그래서 깃허브 블로그 포스팅을 잘 작성하기 위해서 마크다운 문법에 대해서 알고 있으면 좋겠죠?
물론 `HTML` 형식도 지원하긴 합니다.

## 1️⃣ _posts 폴더 만들기
> 📂 폴더 위치: _posts

우선, 포스팅들을 업로드 할 `_posts` 폴더를 만들어 주어야 합니다.
여러분 블로그 레포지토리에 들어가서, `Add file` 이라는 버튼을 누르고, "Create new file" 을 눌러주세요.

[![image.png](https://i.postimg.cc/rmhyBYb2/image.png)](https://postimg.cc/KkMyLQx0)

파일 이름을 입력하는 칸에 `_posts` 를 입력하고, `/` 를 입력하세요.
`/` 를 입력하면 `/` 앞까지 입력했던 글자를 이름으로 하는 폴더가 새로 생긴답니다.

- [![image.png](https://i.postimg.cc/N0Hzqyzs/image.png)](https://postimg.cc/4KX5p3Gq) 
_posts 입력하고,

-  [![image.png](https://i.postimg.cc/qRGQ42XT/image.png)](https://postimg.cc/mzt7Sz5X)
 `/` 입력하기.

그렇게 폴더를 만들어준 후, `연도-월-일-포스팅제목.md` 의 형태로 마크다운 파일을 만들어 주세요. 

## 2️⃣ 포스팅 정보 입력하기
> 📂 작성 위치:  모든 포스팅

단순히 마크다운 형식으로 포스팅을 작성하면 끝나는 것이 아니고, 이 포스팅을 깃허브 블로그가 적용할 수 있도록 정보를 입력해 줘야 합니다.

[![image.png](https://i.postimg.cc/9XZqkyt8/image.png)](https://postimg.cc/PNfxpp7Y)

이렇게 포스팅 파일 위쪽에 `---` 로 구분해서 정보를 작성해 줍니다.

```markdown
---
title:  "포스팅 제목"
excerpt: "포스팅 설명"
categories: 
- 카테고리 1
- 카테고리 2
tags:
- 태그 1
- 태그 2

toc_label: 목차 제목
toc: true
toc_sticky: true
 
date: 2022-02-08
last_modified_at: 2022-02-12
---
```
- title: 포스팅의 제목을 입력합니다
- excerpt: 포스팅의 설명을 입력합니다.

  [![image.png](https://i.postimg.cc/TYThHFP1/image.png)](https://postimg.cc/3WbKkLmQ)
 
  이런식으로 포스팅이 보여질때 설명도 함께 보여집니다. *(이걸로 클릭을 유도할수도...)*

- categories: 카테고리를 입력합니다. 카테고리 개수는 제한이 없지만, 2~3개로 일반화하는 편이 더 나을지도...
- tags: 태그를 입력합니다. 대부분 카테고리보다 더 세부적인 내용을 입력한답니다.
 예) categories: 과일 , tags: 사과
 - toc_label: 목차의 제목을 입력합니다.
 
   [![image.png](https://i.postimg.cc/T2tXf49p/image.png)](https://postimg.cc/XXBPgxtb)
   이런식으로 목차의 제목을 "코드샌드박스'로 정했을 때 예시입니다.
- toc_sticky: 목차가 옆에 달라붙어 있을건지 `true` 나 `false` 로 정합니다.
- date / last_modified_at: 포스팅을 작성한 날짜와 수정한 날짜를 입력합니다.
  
 이건 지극히 기본적인 정보일 뿐이고, 다른 변수들도 있습니다만.... 저는 딱히 관심이 없었습니다. 

## 3️⃣ 포스팅 커밋하기

마크다운 문법을 이용해서 포스팅도 다 썼고, 이것 저것 입력하며 기본 정보도 입력했다면 이제 포스팅이 내 블로그에 나타나 세상의 빛을 볼 수 있도록 해 줘야죠

포스팅 마크다운 파일의 스크롤을 아래로 쭈-욱 내려 주고,
맨 아래 이렇게 `Commit new file` 이라는 초록색 버튼을 클릭해 주면 됩니다.

[![image.png](https://i.postimg.cc/vHKhYY9c/image.png)](https://postimg.cc/6ydnzNMX)

# 💡꿀팁
제가 직접 삽질하며 깃허브 블로그를 만들었다 지웠다 만들었다 지웠다 하며 깨달은 꿀팁들입니다. 여러분은 이런 고생 하지 마세요...
## 1️⃣ URL 은 제대로!
`_config.yml` 파일을 수정할 때, `URL` 을  입력하는 부분이 있는데요.
다른건 몰라도 이 `URL` 부분만큼은 정말 정확하게 입력해야 해요.

블로그 주소 뿐만 아니라 레포지토리 주소도 정확히 입력해야 합니다.
이 주소가 잘못되면 `CSS` 가 깨지거나, `Commit` 을 해도 반영되지 않거나
별별 희한한 오류들을 구경할 수 있습니다.

가장 추천하는 방법은 여러분의 블로그 주소를 `Ctrl + C` 를 눌러 복사해서
 붙여 넣는 것을 가장 추천드려요!
 
## 2️⃣ 적용되는 과정 구경하기
여러분이 이 글을 보고 블로그를 열심히 수정했다고 해도,
 **깃허브**는 꽤 호락호락하지 않습니다. 수정한 내용은 여러분의 블로그에 바로바로 적용되지 않아요. 

저도 처음에는 이것 때문에 *"이게 된건가..."* 하고 뭐가 잘못되진 않았나 궁금했지만
적용이 바로 되지 않아서 정말 답답했습니다. *(오죽했으면 블로그를 지우기까지)*
한번 겪어보신 분들이라면 다 알 거예요.

그렇게 아무거나 막 누르던 와중 발견했습니다.
깃허브의 대박 기능을 말입니다.

[![image.png](https://i.postimg.cc/ht1G8rnx/image.png)](https://postimg.cc/dhDvwGLt)

`Action` 탭에 들어가면

[![image.png](https://i.postimg.cc/y8s1NZRN/image.png)](https://postimg.cc/qzDVbgjf)

이게 적용되는 중인지, 에러가 떴는지 진행 상황이 다 나옵니다.
이걸 구경하다 보면 적용되는걸 기다리는 시간도 금방 가더라고요.
여러분들도 마냥 기다리지 마시고 **Action** 기능 활용해 보세요.

"계속 에러나다가 성공하면 정말 기쁨"
~~~
⊂_ヽ  
　 ＼＼ Λ＿Λ  
　　 ＼( ‘ㅅ’ ) 두둠칫  
　　　 >　⌒ヽ  
　　　/ 　 へ＼  
　　 /　　/　＼＼  
　　 ﾚ　ノ　　 ヽ_つ  
　　/　/두둠칫  
　 /　/|  
　(　(ヽ  
　|　|、＼  
　| 丿 ＼ ⌒)  
　| |　　) /  
`ノ )　　Lﾉ
~~~

## 3️⃣ 코드 쓰기
저처럼 코딩이나 프로그래밍 블로그를 운영하신다 하면 필수적으로 필요한게 **"코드블록"** 입니다. 

이렇게 코드를 넣을 수 있어요.
~~~py
print ("뭘봐?")
요 안에 이렇게 코드를 넣을 수 있지요오오오~~~~
~~~

이 기능은 마크다운 문법의 일종입니다.
~~~markdown
```py
여기는 파이썬 코드!
```
```markdown
여기는 마크다운 코드!
```
```ruby
여기는 루비 코드!
```
~~~

이렇게
~~~markdown
[```] 이나 [~~~]
~~~
를 입력하고, 언어 종류를 써 준 다음 안에 코드를 작성하면 코드를 나타낼 수 있어요. (색칠까지 된 상태로요!)

이렇게 나타내는게 못마땅하거나, 쓰고 싶지 않으시다면

👉 [https://gist.github.com/](https://gist.github.com/)

👉 [https://carbon.now.sh/](https://carbon.now.sh/)

👉 [https://colorscripter.com/](https://colorscripter.com/)


이런걸 이용해서 코드를 작성하시면 될 것 같네요.

# 참고한 블로그들
이러한 내용을 알게 해주셔서 (감사합니다) 

- [https://eona1301.github.io/categories/](https://eona1301.github.io/categories/)
- 
- [https://ansohxxn.github.io/blog/posting/](https://ansohxxn.github.io/blog/posting/)



👀 또 다른 깃허브 블로그 꿀팁들을 보고 싶다면 [👉깃허브 카테고리](https://eggjini.github.io/categories/#github)를 참고하세요!
{: .notice--success} 
