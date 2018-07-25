---
theme : "night"
highlightTheme: "darkula"
customTheme : "reveal-custom-theme"
transition: "slide"
transitionSpeed: 'slow'
---

# vscode 에서 revealjs 사용

- vscode : https://code.visualstudio.com/
- revealjs : https://revealjs.com

note:

- **visual studio 코드**에서 **revealjs** 를 사용하는 법을 알아보겠습니다.
- reveal.js 프레임워크만을 가지고 프리젠테이션을 만들 수 있습니다.
- 그러기 위해서는 node 를 설치하고 명령어를 입력해야 하는 번거로움이 있습니다.
- vscode 를 통해서 쉽게 사용해 보도록 하겠습니다.

--

## vscode?

![](https://goo.gl/SjgQP2)

비주얼 스튜디오 코드(영어: Visual Studio Code)는 마이크로소프트가 마이크로소프트 윈도우, macOS, 리눅스용으로 개발한 소스 코드 편집기

<p>출처: 위키피디아</p><!--.element: class="small"-->

note:

- vscode 에 대해서 먼저 살펴보겠습니다.
- 위키피디아예서 비주얼 스튜디오 코드(영어: Visual Studio Code)는 마이크로소프트가 마이크로소프트 윈도우, macOS, 리눅스용으로 개발한 소스 코드 편집기로 설명되어 있습니다.
- 제가 요즘 가장 많이 사용하는 에디터가 **vscode** 입니다.
- 중요한 것은 **무료**라는 것입니다.
- 그리고 어느 플랫폼에서도 사용할 수 있는 장점이 있습니다.
- 크로스플랫폼으로 윈도우, 리눅스, 맥을 모두 지원합니다.
- 비슷한 에디터로는 github 에서 만든 **Atom** 이 있습니다.

--

### vscode 설치

https://code.visualstudio.com/

![Download VSCODE](https://goo.gl/9tqrFw)

note:

- 홈페이지에서 다운로드 받아서 vscode 를 설치합니다.
- 설치는 기본값으로 진행하면 됩니다.
- 설치가 되어있자면 다음 단계로 진행하시면 됩니다.

--

### vscode 실행 화면

![](https://goo.gl/YCHYYe)

note:

- 설치된 vscode 를 실행을 하면 이와 같은 첫페이지를 볼 수 있습니다.

--

## reveal?

![](https://goo.gl/SEjNaz)

홈페이지: https://revealjs.com

HTML 프리젠테이션 프레임워크

note:

- reveal js 는 HTML 을 이용하여 프리젠테이션을 할 수 있는 프레임워크입니다.
- html 로 작성하면 다양한 형태로 작성이 가능하지만 html 문법을 알아야 하는 합니다.
- 다행히 reveal 에서 markdown 을 지원하기 때문에 마크다운으로 문서를 작성하면 쉽게 프리젠테이션 문서를 만들 수 있습니다.

---

## 확장 설치

vscode 에서 확장 `vscode-reveal` 설치

단축키 : Ctrl + Shift + X

![](https://goo.gl/bBgdvG)

note:

- vscode 에서 reveal 을 사용하기 위해 **vscode-reveal** 확장을 설치합니다.
- 왼쪽 메뉴에서 위에서 다섯번째에 있는 확장을 선택합니다.
- 단축키는 **Ctrl + Shift + X** 입니다.
- 여기에서 revealjs 를 검색합니다.

--

### 확장 설치 확인

![](https://goo.gl/okH3DE)

1.  html 파일로 출력
2.  pdf 파일로 출력
3.  브라우저에서 미리보기
4.  사이드에서 미리보기

note:

- vscode 의 탐색기 패널에 **SLIDES** 가 생긴것을 확인할 수 있습니다.
- 이제부터 reveal.js 를 사용할 수 있습니다.
- slides 패널 상단 우측에 보이는 각각의 버튼은 다음과 같습니다.
  1.  html 파일로 출력
  2.  pdf 파일로 출력
  3.  브라우저에서 미리보기
  4.  사이드에서 미리보기

---

## Markdown

- 마크다운 문서 작성

<hr>
#### 참고 링크

- https://www.markdownguide.org/basic-syntax
- https://guides.github.com/features/mastering-markdown/

note:

- 마크다운으로 문서를 작성하기에 기본적인 문법을 알고 있어야 합니다.
- 마크다운 문법을 사용하여 헤더, 리스트, 이미지 등등을 작성합니다.
- https://www.markdownguide.org/basic-syntax 에서 기본 문법을 확인 할 수 있습니다.
- 이 곳 외에 검색을 하면 다양한 곳에서 확인 할 수 있습니다.
- github 에서도 마크다운을 지원하며, 문법 관련 문서도 확인할 수 있습니다.

--

### 헤더

```
# Heading level 1
## Heading level 2
### Heading level 3
```

# Heading level 1

## Heading level 2

### Heading level 3

note:

- 먼저 헤더를 작성하는 법을 알아보겠습니다.
- 샵을 입력하여 헤더를 작성합니다.

--

### 순서 있는 리스트

입력

```
1. First item
2. Second item
3. Third item
4. Fourth item
```

<hr>
결과

1.  First item
2.  Second item
3.  Third item
4.  Fourth item

note:

- 순서가 있는 리스트는
- 숫자를 입력하고 .(점)을 붙여쓰고 한칸을 띄어줍니다.

--

### 순서 없는 리스트

입력

```
- First item
- Second item
- Third item
- Fourth item
```

<hr>
결과

- First item
- Second item
- Third item
- Fourth item

note:

- 순서가 없는 리스트의 경우에는
- 대쉬(-)를 입력하고 한칸을 띄어줍니다.

--

## 이미지

```
![Tux, the Linux mascot](https://upload.wikimedia.org/wikipedia/commons/thumb/3/35/Tux.svg/100px-Tux.svg.png)
```

![Tux, the Linux mascot](https://upload.wikimedia.org/wikipedia/commons/thumb/3/35/Tux.svg/100px-Tux.svg.png)

```
![](https://upload.wikimedia.org/wikipedia/commons/thumb/3/35/Tux.svg/100px-Tux.svg.png)
```

https://upload.wikimedia.org/wikipedia/commons/thumb/3/35/Tux.svg/100px-Tux.svg.png

note:

- 이미지를 보여주는 마크다운 문법입니다.
- 느낌표 뒤에 대괄호로 이미지의 설명을 입력하고, 괄호안에 이미지의 주소를 입력합니다.
- 이미지의 설명은 생략될 수 있습니다.

--

## 코드 작성

예제코드

<pre>
```python
new_list = []
for i in old_list:
    if filter(i):
        new_list.append(expressions(i))
```
</pre>

- https://highlightjs.org/
- 176 languages and 79 styles

note:

- 어퍼스트로피 3 개를 이어서 작성하여 코드 블럭의 시작과 끝을 표시합니다.
- 시작부분에 코드의 언어를 지정합니다.
- 지정할 수 있는 언어의 목록은 https://highlightjs.org/ 에서 확인 할 수 있습니다.
- 내부적으로 hightlightjs 를 사용하고 있으므로, 여기서 제공하는 176 가지 언어와 79 가지의 스타일을 지정할 수 있습니다.

---

## 작성

helloworld.md 파일 생성

```
# Hello World

- First item
- Second item
- Third item
- Fourth item

![](https://code.visualstudio.com/assets/images/home-intellisense.svg)
```

note:

- 먼저 간단한 문서를 만들고 테스트 해보겠습니다.
- 새 문서를 만들고, helloworld.md 로 이름을 변경합니다.
- 확장자를 **md** 로 지정합니다.
- md 는 마크다운을 의미합니다.
- 내용에는
- 위와 같이 #(샵) 한칸 띄어쓰고 Hello World 를 입력합니다.

---

## 기능확인

![](https://goo.gl/okH3DE)

1.  html 파일로 출력
2.  pdf 파일로 출력
3.  브라우저에서 미리보기
4.  사이드에서 미리보기

--

### html 출력

![](https://goo.gl/7uzgPe)

- /helloworld-export 폴더
- /helloworld-export/index.html 파일

```html
<div class="reveal">
            <div class="slides"><section  data-markdown><script type="text/template"># Hello World

- First item
- Second item
- Third item
- Fourth item

![](https://code.visualstudio.com/assets/images/home-intellisense.svg)
</script></section></div>
```

note:

- 작성한 마크다운 파일이 있는 곳에 helloworld-export 폴더가 생성됩니다.
- 그리고 그 안에 들어가 보면 프리젠테이션을 위한 파일들이 생성되어 있는 것을 확인할 수 있습니다.
- 여기서 index.html 파일이 작성한 프리젠테이션 파일입니다.
- 파일의 내용을 열어보면 작성한 내용을 확인할 수 있습니다.
- revealjs 만들 사용하여 만들경우 위와 같은 내용을 직접 작성해주면 됩니다. 조금더 작성해야 할 내용이 늘어나게 됩니다.

--

## 미리보기

![](https://goo.gl/xrBRFJ)

먼저 SLIDES 에 있는 버튼 중 가장 오른쪽 버튼을 눌러서 **오른쪽 사이드에서 미리보기**를 실행합니다.

![](https://goo.gl/hYQXXf)

한페이지에 모두 나오게 되므로, 페이지 분할이 필요합니다.

---

## 페이지 분할

- **---** : 수평분할
- **--** : 수직분할

![](https://goo.gl/TNKNRf)

note:

- **---** 를 사용하여 수평분할, **--** 를 사용하여 수직분할 할 수 있습니다.
- 기본적으로 대쉬 3 개를 사용하여 수평분할로 페이지를 작성합니다. 수평분할된 페이지는 오른쪽으로 이동합니다.
- 세부내용의 페이지를 작성할 경우 대쉬 2 개를 사용하여 페이지를 작성합니다. 이때 페이지는 아래쪽으로 이동합니다.
- 화면 오른쪽 아래위치에
- 수평으로 페이지가 더 있으면 오른쪽 화살표가 나타나며
- 수직으로 페이지가 더 있으면 아래쪽 화살표가 나타납니다.

--

### 수평 분할

![](https://lh3.googleusercontent.com/-roqz5ipfyyE/W1hZYYW1kVI/AAAAAAAAGyU/1aZL6WNA-QUXh4oAwPnp5HnwiS6QKBEhACHMYCw/s0/StrokesPlus_2018-07-25_3.png)

**---** 를 입력하여 페이지 분할

![](https://lh3.googleusercontent.com/-GOzUONPZ1Sw/W1hYjH1UhHI/AAAAAAAAGyE/3FbQ9AU3VsgVEEZ9pynXv5DdnJMRzlCcQCHMYCw/s0/StrokesPlus_2018-07-25_1.png)

note:

- --- 사용하여 페이지를 분할하면
- SLIDES 패널에서 다음과 같은 목록을 볼 수 있습니다.

--

### 수직 분할

**--** 를 사용하여 수직분할

![](https://lh3.googleusercontent.com/-iGKuF499b1M/W1haA8MzH2I/AAAAAAAAGyg/KCC8jPTu6AAXj4zFoZHv9yXb7QowW2ggQCHMYCw/s0/StrokesPlus_2018-07-25_4.png)<!-- .element: class="left"-->

![](https://lh3.googleusercontent.com/-pgZr6SUcv6Y/W1hYn6ZPV2I/AAAAAAAAGyI/jASUdyuZ39Qnj1tay-GIkozit1mgEaTMACHMYCw/s0/StrokesPlus_2018-07-25_2.png)<!-- .element: class="right"-->

우측 하단 화살표<!-- .element: class="center"-->

![](https://lh3.googleusercontent.com/-ktdQcGb3OTg/W1gr-GfpWWI/AAAAAAAAGxY/V4lvmpN_5H0LmRfQEJNSMl3ilOni-B_WgCHMYCw/s0/StrokesPlus_2018-07-25_16-51-30.png)

note:

- **--** 를 사용하여 수직분할하면 해당 페이지 하위로 구분됩니다.
- 페이지를 분할하면 우측 하단에 화살표가 생긴것을 확인할 수 있습니다.
- 하위 페이지가 있는 경우 아래 화살표가 생깁니다.

---

## 애니메이션

<span class="fragment">... a</span> <span class="fragment">fragmented</span> <span class="fragment">slide.</span>

grow <!-- .element: class="fragment grow" -->

shrink <!-- .element: class="fragment shrink" -->

fade-out <!-- .element: class="fragment fade-out " -->

fade-up (also down, left and right!) <!-- .element: class="fragment fade-up" -->

current-visible <!-- .element: class="fragment current-visible" -->

Highlight <span class="fragment highlight-red">red</span> <span class="fragment highlight-blue">blue</span> <span class="fragment highlight-green">green</span>

<div>출처: https://raw.githubusercontent.com/evilz/vscode-reveal/master/sample.md</div><!-- .element: class="small"-->

note:

- 애니메이션에 어떤 것이 있는지 먼저 확인해 보겠습니다.
- 하나씩 나타나는 것
- 커지고 작아지고 사라지고 나타나는 것
- 색을 변경할 수 있습니다.

--

### 글자 단위

입력

```
<span class="fragment">... a</span>
<span class="fragment">fragmented</span>
<span class="fragment">slide.</span>
```

<hr>

결과

- ... a
- fragmented
- slide.

<hr>

```
<span class="fragment">... a</span><span class="fragment">fragmented</span><span class="fragment">slide.</span>
```

note:

- 이렇게 작성하면 다음 내용들이 순차적으로 나타나게 됩니다.
- span 태그로 작성되어 있기때문에 옆으로 붙여서 작성할 수도 있습니다.

--

### 색상변경

```html
Highlight
<span class="fragment highlight-red">red</span>
<span class="fragment highlight-blue">blue</span>
<span class="fragment highlight-green">green</span>
```

Highlight

<span class="fragment highlight-red">red</span>
<span class="fragment highlight-blue">blue</span>
<span class="fragment highlight-green">green</span>

note:

- 이렇게 작성하면 각각의 red, blue, green 의 글자색이 변경됩니다.
- span 태그를 사용하여 작성합니다.
- class 에 fragment 를 추가합니다.
- 그리고 클래스에 변경될 색상을 작성합니다.
- 사전에 정의된 hightligh-red, highlight-blue, hightlight-green 을 사용할 수 있습니다.

--

### html 주석

```
<!-- 주석 내용 -->
```

예제

```
<!-- 본문 시작 -->
<div class="main-article">
  ...
</div>
<!-- 본문 끝 -->
```

<!-- 주석 내용 -->

note:

- 문단 단위로 애니메이션을 지정할 수 있습니다.
- 확대, 축소, 사라지기, 나타나기 를 표현할 수 있습니다.
- 작성은 html 주석 코드를 사용합니다.
- Left Angle Braket 느낌표, 대쉬 2 개 로 열고
- 대쉬 2 개 Right Angle Braket 로 닫습니다.
- 이렇게 작성한 내용은 발표화면에 표시되지 않습니다.

--

### 문단 단위

```html
grow(확대) <!-- .element: class="fragment grow" -->

shrink(축소) <!-- .element: class="fragment shrink" -->

fade-out(사라지기) <!-- .element: class="fragment fade-out " -->

fade-up(나타내기)<!-- .element: class="fragment fade-up" -->

current-visible(현재만 보이기) <!-- .element: class="fragment current-visible" -->
```

grow(확대) <!-- .element: class="fragment grow" -->

shrink(축소) <!-- .element: class="fragment shrink" -->

fade-out(사라지기) <!-- .element: class="fragment fade-out " -->

fade-up(나타내기) <!-- .element: class="fragment fade-up" -->

current-visible(현재만 보이기) <!-- .element: class="fragment current-visible" -->

note:

- html 주석을 사용하여
- 확대, 축소, 사라지기, 나타내기를 지정합니다.

--

### fade-in

```
위<!-- .element: class="fragment fade-up" -->

아래<!-- .element: class="fragment fade-down" -->

왼쪽<!-- .element: class="fragment fade-left" -->

오른쪽<!-- .element: class="fragment fade-right" -->
```

위<!-- .element: class="fragment fade-up" -->

아래<!-- .element: class="fragment fade-down" -->

왼쪽<!-- .element: class="fragment fade-left" -->

오른쪽<!-- .element: class="fragment fade-right" -->

note:

- 나타나기는 위,아래,좌,우 모두 선택할 수 있습니다.
- 클래스로 지정한 fade-up 위치에 fade-down, fade-left, fade-right 를 입력하여 작성합니다.

---

## 배경 변경

- 색상 변경
- 이미지 변경

note:

- 테마를 통해서 전체 슬라이드의 배경 색상을 변경할 수 있지만
- 각각 페이지에 배경 색상 지정을 통해서도 변경할 수 있습니다.
- 또는 이미지를 배경으로 넣을 수 있습니다

--

<!-- .slide: data-background="#006064" -->

### 배경 색상

RGB

```
<!-- .slide: data-background="#006064" -->
```

hsla

```
<!-- .slide: data-background="hsla(0,100%,50%,0.5)" -->
```

note:

- html 주석 코드를 사용하여 색상을 지정합니다.
- 16 진수 RGB 값을 이용하여 색상을 지정할 수 있으며
- Hue-saturation-lightness-alpha 모델인 hsla 를 사용해서도 색상을 지정할 수 있습니다.
- 현재 페이지는 위에 있는 RGB 코드를 사용하여 작성하였습니다.

--

<!-- .slide: data-background="https://goo.gl/UfMdw8" data-background-transition="slide" -->

### 배경 이미지

```html
<!-- .slide: data-background="https://goo.gl/UfMdw8"  -->
```

<br>
<br>

배경 이미지가 벗어나는 경우 custom-theme 사용

```html
.reveal div.slide-background.present {
  background-size: contain;
}
```

note:

- html 주석 코드를 사용하여 이미지를 지정합니다.
- 이미지의 크기가 큰 경우 화면을 벗어나게 되는데 이때는 custom-theme 를 적용하여 페이지 안에 모두 들어오게 작성할 수 있습니다.
- 뒤에서 커스텀 테마를 작성하겠습니다.

---

## 속성 지정

![](https://lh3.googleusercontent.com/-4ce82-Cmr5M/W1gosDcyLLI/AAAAAAAAGxM/iW-krCR2cMQSnlxvp6Pu_DkdtbW8gI6mwCHMYCw/s0/StrokesPlus_2018-07-25_16-37-31.png)

```yml
theme : "night"
highlightTheme: "darkula"
customTheme : "reveal-custom-theme"
transition: "slide"
transitionSpeed: 'slow'
```

note:

- 문서 상단에 속성을 지정할 수 있습니다.
- 대쉬 3 개를 사용하여 속성의 시작과 종료를 지정합니다.

---

## 테마

```
theme : "night"
```

테마 목록

- black
- white
- league
- sky
- beige
- simple
- serif
- blood
- night
- moon
- solarized

note:

- 문서 상단에 지정하는 속성을 이용하여 테마를 지정합니다.
- night 외에, black, white, league, sky, beige, simple, serif, blood, night, moon, solarized,
- 기본은 black 으로 지정되어 있습니다.
- 각각의 모습은 테마를 변경해 보면서 확인할 수 있습니다.

--

### 테마 확인

아래 링크를 누르면 테마가 변경됩니다.

<a href="#" onclick="document.getElementById('theme').setAttribute('href','css/theme/black.css'); return false;">Black (default)</a> -
<a href="#" onclick="document.getElementById('theme').setAttribute('href','css/theme/white.css'); return false;">White</a> -
<a href="#" onclick="document.getElementById('theme').setAttribute('href','css/theme/league.css'); return false;">League</a> -
<a href="#" onclick="document.getElementById('theme').setAttribute('href','css/theme/sky.css'); return false;">Sky</a> -
<a href="#" onclick="document.getElementById('theme').setAttribute('href','css/theme/beige.css'); return false;">Beige</a> -
<a href="#" onclick="document.getElementById('theme').setAttribute('href','css/theme/simple.css'); return false;">Simple</a> <br>
<a href="#" onclick="document.getElementById('theme').setAttribute('href','css/theme/serif.css'); return false;">Serif</a> -
<a href="#" onclick="document.getElementById('theme').setAttribute('href','css/theme/blood.css'); return false;">Blood</a> -
<a href="#" onclick="document.getElementById('theme').setAttribute('href','css/theme/night.css'); return false;">Night</a> -
<a href="#" onclick="document.getElementById('theme').setAttribute('href','css/theme/moon.css'); return false;">Moon</a> -
<a href="#" onclick="document.getElementById('theme').setAttribute('href','css/theme/solarized.css'); return false;">Solarized</a>

note:

- 아래 링크를 누르면 테마가 변경됩니다.

---

## 하이라이트 테마

```yml
highlightTheme: "darkula"
```

https://highlightjs.org/static/demo/

![](https://lh3.googleusercontent.com/-G4i0quIB6wg/W1gvRZF4KNI/AAAAAAAAGxo/5O_ZzodrTqg0rlXYXGMLRkC0ckpicbcUACHMYCw/s0/StrokesPlus_2018-07-25_17-05-35.png)

note:

- 코드 블럭의 하이라이트 테마를 지정할 수 있습니다.
- https://highlightjs.org/static/demo/ 에서 79 가지 코드 테마를 확인할 수 있습니다.

---

### 사용자 정의 테마

reveal-custom-theme.css 파일 생성

greenyellow 색상 추가

```css
.reveal .greenyellow {
  color: greenyellow;
}
```

--

### 사용자 정의 적용

```
그린옐로우 색상 적용<!-- .element: class="fragment fade-up greenyellow"-->
```

적용한 클래스

- fragment
- fade-up
- greenyello

<hr>

그린옐로우 색상 적용<!-- .element: class="fragment fade-up greenyellow"-->

note:

- css 파일을 추가하여 사용자 정의 테마를 만들 수 있습니다.
- reveal-custom-theme.css 파일을 생성합니다.
- 파일명은 원하시는 것으로 바꿀 수 있습니다.
- 사용할 때 파일명만 정확하게 입력하면 됩니다.
- greenyellow 색상을 추가하겠습니다.
- 클래스명을 greenyellow 로 주었습니다.
- html 주석 코드를 사용하여 생성한 클래스를 적용합니다.

--

### 테마 조합

![](https://lh3.googleusercontent.com/-4ce82-Cmr5M/W1gosDcyLLI/AAAAAAAAGxM/iW-krCR2cMQSnlxvp6Pu_DkdtbW8gI6mwCHMYCw/s0/StrokesPlus_2018-07-25_16-37-31.png)

```yml
theme : "night"
highlightTheme: "darkula"
customTheme : "reveal-custom-theme"
transition: "slide"
```

note:

- theme, highlighTheme, customTheme, transition 을 정의하였습니다.

---

## 발표

- ESC : Overview mode
- 이동키 : 상하좌우로 페이지 이동
- 스페이스바 : 다음 페이지로 이동
- S : 스피커 노트

note:

- 프리젠테이션 발표시 ESC, 이동키, 스페이스바, S 키를 사용할 수 있습니다.

--

### ESC

![](https://lh3.googleusercontent.com/-Z5UxKMNDPA4/W1hXQicqjMI/AAAAAAAAGx4/m11kX5oB9r4tyvgy_RbkEHVVL3qax_5bACHMYCw/s0/StrokesPlus_2018-07-25_19-56-12.png)

note:

- ESC 키를 누르면 overview mode 로 전환됩니다.
- 이 화면에서 페이지를 선택하면 해당 페이지로 이동하고
- ESC 키를 누르면 원래 페이지로 이동합니다.

---

## 참고

- https://www.markdownguide.org/basic-syntax
- https://revealjs.com
- https://raw.githubusercontent.com/evilz/vscode-reveal/master/sample.md
- https://dymaxionkim.github.io/beautiful-jekyll/2017-01-25-Revealjs/
- https://highlightjs.org/
