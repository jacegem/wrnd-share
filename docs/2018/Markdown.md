---
customTheme : "my-theme"
theme : "night"
transition: "slide"
transitionSpeed: 'slow'
highlightTheme: "darkula"
---

<!-- .slide: data-background="https://goo.gl/RU8eA5" data-background-transition="slide" -->

## Markdown 이란?

<div>

**Markdown**은 텍스트 기반의 마크업언어

마크다운이 최근 각광받기 시작한 이유는 깃헙(https://github.com) 덕분이다. 

**README.md**는 깃헙을 사용하는 사람이라면 누구나 가장 먼저 접하게 되는 마크다운 문서였다. 
</div><!-- .element: class="fragment fade-up"-->

<div>출처: https://gist.github.com/ihoneymon/652be052a0727ad59601</div><!-- .element: class="small"-->

---

<!-- .slide: data-background="https://goo.gl/GF9kXi" data-background-transition="slide" -->

![](https://goo.gl/t9RSx6?.png)<!-- .element: class="fragment fade-up"-->

---

<!-- .slide: data-background="https://goo.gl/r4ui8F" data-background-transition="slide" -->

## README.md

```markdown
<div align="center">
  <img src="https://www.tensorflow.org/images/tf_logo_transp.png"><br><br>
</div>

-----------------

| **`Linux CPU`**                                                                                                                              | **`Linux GPU`**                                                                                                                                          | **`Mac OS CPU`**                                                                                                                             | **`Windows CPU`**                                                                                                                                              | **`Android`**                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [![Build Status](https://ci.tensorflow.org/buildStatus/icon?job=tensorflow-master-cpu)](https://ci.tensorflow.org/job/tensorflow-master-cpu) | [![Build Status](https://ci.tensorflow.org/buildStatus/icon?job=tensorflow-master-linux-gpu)](https://ci.tensorflow.org/job/tensorflow-master-linux-gpu) | [![Build Status](https://ci.tensorflow.org/buildStatus/icon?job=tensorflow-master-mac)](https://ci.tensorflow.org/job/tensorflow-master-mac) | [![Build Status](https://ci.tensorflow.org/buildStatus/icon?job=tensorflow-master-win-cmake-py)](https://ci.tensorflow.org/job/tensorflow-master-win-cmake-py) | [![Build Status](https://ci.tensorflow.org/buildStatus/icon?job=tensorflow-master-android)](https://ci.tensorflow.org/job/tensorflow-master-android) |

**TensorFlow** is an open source software library for numerical computation using
data flow graphs.  The graph nodes represent mathematical operations, while
the graph edges represent the multidimensional data arrays (tensors) that flow
between them.  This flexible architecture lets you deploy computation to one
or more CPUs or GPUs in a desktop, server, or mobile device without rewriting
code.  TensorFlow also includes TensorBoard, a data visualization toolkit.

TensorFlow was originally developed by researchers and engineers
working on the Google Brain team within Google's Machine Intelligence Research
organization for the purposes of conducting machine learning and deep neural
networks research.  The system is general enough to be applicable in a wide
variety of other domains, as well.

**If you want to contribute to TensorFlow, be sure to review the [contribution
guidelines](CONTRIBUTING.md). This project adheres to TensorFlow's
[code of conduct](CODE_OF_CONDUCT.md). By participating, you are expected to
uphold this code.**

**We use [GitHub issues](https://github.com/tensorflow/tensorflow/issues) for
tracking requests and bugs. So please see 
[TensorFlow Discuss](https://groups.google.com/a/tensorflow.org/forum/#!forum/discuss) for general questions
and discussion, and please direct specific questions to [Stack Overflow](https://stackoverflow.com/questions/tagged/tensorflow).**

.. 이하 생략 ..
```

<div>출처: https://raw.githubusercontent.com/tensorflow/tensorflow/master/README.md</div><!-- .element: class="small"-->

---

<!-- .slide: data-background="https://goo.gl/kdDSSD" data-background-transition="slide" -->

## 마크다운의 장점

<div>1. **간결**하다.</div><!-- .element: class="fragment fade-up"-->
<div>2. 별도의 도구없이 작성가능하다.</div><!-- .element: class="fragment fade-up"-->
<div>3. 다양한 형태로 변환이 가능하다.</div><!-- .element: class="fragment fade-up"-->
<div>4. **텍스트(Text)**로 저장되기 때문에 용량이 적어 보관이 용이하다.</div><!-- .element: class="fragment fade-up"-->
<div>5. 텍스트파일이기 때문에 **버전관리**시스템을 이용하여 변경이력을 관리할 수 있다.</div><!-- .element: class="fragment fade-up"-->
<div>6. 지원하는 프로그램과 플랫폼이 다양하다.</div><!-- .element: class="fragment fade-up"-->


---
<!-- .slide: data-background="https://goo.gl/oTU4WP" data-background-transition="slide" -->

## 마크다운의 단점

<div>1. **표준이 없다**.</div><!-- .element: class="fragment fade-up"-->
<div>2. 표준이 없기 때문에 도구에 따라서 변환방식이나 생성물이 다르다.</div><!-- .element: class="fragment fade-up"-->
<div>3. **모든 HTML 마크업을 대신하지 못한다**.</div><!-- .element: class="fragment fade-up"-->



---
<!-- .slide: data-background="https://goo.gl/6HkCZp" data-background-transition="slide" -->

## 마크다운 사용법

- Headers 해더
- BlockQuote 인용구
- list 목록
- code 코드
- link 링크
- strong 강조
- image 이미지

<div>출처: https://gist.github.com/ihoneymon/652be052a0727ad59601</div><!-- .element: class="small"-->


---
<!-- .slide: data-background="https://goo.gl/eccY3q" data-background-transition="slide" -->

## Headers 해더

<div>
입력
```html
# This is a H1
## This is a H2
### This is a H3
#### This is a H4
##### This is a H5
###### This is a H6
```
</div><!-- .element: class="fragment fade-up"-->

<div>
결과
# This is a H1
## This is a H2
### This is a H3
#### This is a H4
##### This is a H5
###### This is a H6
</div><!-- .element: class="fragment fade-up"-->


---
<!-- .slide: data-background="https://goo.gl/r4ui8F" data-background-transition="slide" -->

## BlockQuote 인용구

<div>
입력
```html
> This is a blockqute.
```
</div><!-- .element: class="fragment fade-up"-->

<div>
결과
> This is a blockqute.

</div><!-- .element: class="fragment fade-up"-->

---

<!-- .slide: data-background="https://goo.gl/C7NU1B" data-background-transition="slide" -->

## list 목록

<div>
입력
```html
- 첫번째
- 두번째
- 세번째
```
</div><!-- .element: class="fragment fade-up"-->

<div>
결과

- 첫번째
- 두번째
- 세번째
</div><!-- .element: class="fragment fade-up"-->

---

<!-- .slide: data-background="https://goo.gl/wVUN2y" data-background-transition="slide" -->

## code 코드

<div>

입력

\`\`\`<br>
This is a code block.<br>
\`\`\`

</div><!-- .element: class="fragment fade-up"-->

<div>
결과

```html
This is a code block.
```
</div><!-- .element: class="fragment fade-up"-->


---
<!-- .slide: data-background="https://goo.gl/exp8sA" data-background-transition="slide" -->

## link 링크

<div>

입력
```html
syntax: [Title](link)

[google](https://www.google.co.kr)
```
</div><!-- .element: class="fragment fade-up"-->

<div>

결과

syntax: [Title](link)

[google](https://www.google.co.kr)
</div><!-- .element: class="fragment fade-up"-->


---
<!-- .slide: data-background="https://goo.gl/pNd8TA" data-background-transition="slide" -->

## strong 강조

<div>

입력
```md
*single asterisks*
_single underscores_
**double asterisks**
__double underscores__
++underline++
~~cancelline~~
```
</div><!-- .element: class="fragment fade-up"-->

<div>

결과

*single asterisks*

_single underscores_

**double asterisks**

__double underscores__

++underline++

~~cancelline~~
</div><!-- .element: class="fragment fade-up"-->


---
<!-- .slide: data-background="https://goo.gl/vTvRVr" data-background-transition="slide" -->

## image 이미지

<div>

입력
```html
![Rubber Duck](https://goo.gl/BKYB1D)
```
</div><!-- .element: class="fragment fade-up"-->

<div>

결과

![Rubber Duck](https://goo.gl/BKYB1D)
</div><!-- .element: class="fragment fade-up"-->


---
<!-- .slide: data-background="https://goo.gl/C7NU1B" data-background-transition="slide" -->

## 마크다운을 사용할 수 있는 Site

### Github 

![](https://goo.gl/YfUcCD)


---
<!-- .slide: data-background="https://goo.gl/wVUN2y" data-background-transition="slide" -->

### Gitbook

![](https://goo.gl/n3CfeS)


---
<!-- .slide: data-background="https://goo.gl/pNd8TA" data-background-transition="slide" -->

## 마크다운을 사용할 수 있는 Application

### Typora

![](https://goo.gl/W16WtG)


---
<!-- .slide: data-background="https://goo.gl/exp8sA" data-background-transition="slide" -->

### BoostNote

![](https://goo.gl/uzotV2)

---

<!-- .slide: data-background="https://goo.gl/RU8eA5" data-background-transition="slide" -->

## 마크다운 온라인 실습

- https://dillinger.io/
- https://stackedit.io/
- http://jbt.github.io/markdown-editor/

---

<!-- .slide: data-background="https://goo.gl/vTvRVr" data-background-transition="slide" -->

## 감사합니다.

![](https://goo.gl/EhZmMR)









