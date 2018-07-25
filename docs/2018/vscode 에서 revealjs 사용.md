---
customTheme : "reveal-custom-theme"
theme : "night"
transition: "slide"
transitionSpeed: 'slow'
highlightTheme: "darkula"
---

# vscode 에서 revealjs 사용

note:

- visual studio 코드에서 revealjs 를 사용하는 법을 알아보겠습니다.
- revealjs 만들가지고 사용할 수도 있지만, vscode 를 통해서 쉽게 프리젠테이션을 만들어 보겠습니다.

--

## vscode?

![](https://goo.gl/SjgQP2)

비주얼 스튜디오 코드(영어: Visual Studio Code)는 마이크로소프트가 마이크로소프트 윈도우, macOS, 리눅스용으로 개발한 소스 코드 편집기

<p>출처: 위키피디아</p><!--.element: class="small"-->

note:

- vscode 란 무엇인가?
- 위키피디아예서 비주얼 스튜디오 코드(영어: Visual Studio Code)는 마이크로소프트가 마이크로소프트 윈도우, macOS, 리눅스용으로 개발한 소스 코드 편집기로 설명되어 있습니다.
- 제가 요즘 가장 많이 사용하는 에디터 입니다.
- 중요한 것은 **무료**라는 것입니다.
- 그리고 어느 플랫폼에서도 사용할 수 있습니다.
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

### 기능확인

![](https://goo.gl/okH3DE)

1.  html 파일로 출력
2.  pdf 파일로 출력
3.  브라우저에서 미리보기
4.  사이드에서 미리보기

--

## 미리보기

![](https://goo.gl/xrBRFJ)

먼저 SLIDES 에 있는 버튼 중 가장 오른쪽 버튼을 눌러서 **오른쪽 사이드에서 미리보기**를 실행합니다.

![](https://goo.gl/hYQXXf)

한페이지에 모두 나오게 되므로, 페이지 분할이 필요합니다.

---

## 페이지 분할

**---** 를 사용하여 수평분할, **--** 를 사용하여 수직분할 할 수 있습니다.

먼저 **---** 를 입력하여 페이지를 분할하면, 페이지 목록을 SLIDES 패널에서 확인할 수 있습니다.

![](https://goo.gl/Pyunpf)

**--** 를 사용하여 수직분할하면 해당 페이지 하위로 구분됩니다.

![](https://goo.gl/YndSSF)

페이지를 분할한 이후에 미리보기를 화면 우측 하단에 화살표가 생긴것을 확인할 수 있습니다. 하위 페이지가 있는 경우 아래 화살표가 생깁니다.

![](https://goo.gl/ZJBqYH)

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
Highlight <span class="fragment highlight-red">red</span> <span class="fragment highlight-blue">blue</span> <span class="fragment highlight-green">green</span>
```

### 줄 단위

```html
grow <!-- .element: class="fragment grow" -->

shrink <!-- .element: class="fragment shrink" -->

fade-out <!-- .element: class="fragment fade-out " -->

fade-up (also down, left and right!) <!-- .element: class="fragment fade-up" -->

current-visible <!-- .element: class="fragment current-visible" -->
```

fragment 클래스를 주고 추가적인 액션을 정의 합니다.

- grow
- shrink
- fade-out
- fase-up, down, left, right
- current-visible

---

## 배경 변경

### 색상

### 이미지

---

## 테마

--

## 노트 작성

**showNotes** 속성 을 정의합니다.

```
showNotes: "true";
```

기본값은 false 이므로 작성하지 않아도 됩니다.

```
showNotes: "false";
```

note:

- 노트에 작성을 하면 발표자만 확인할 수 있습니다.
- 옵션을 작성하여 모두 보이게도 할 수 있습니다.
- 기본값은 **false** 이므로 작성하지 않아도 됩니다.

---

## 발표

ESC
이동키,
스페이스바

---

## 참고

- https://www.markdownguide.org/basic-syntax
- https://revealjs.com
- https://raw.githubusercontent.com/evilz/vscode-reveal/master/sample.md
- https://dymaxionkim.github.io/beautiful-jekyll/2017-01-25-Revealjs/
