---
customTheme : "my-theme"
theme : "night"
transition: "slide"
transitionSpeed: 'slow'
highlightTheme: "darkula"
---

<!-- .slide: data-background="#006064" data-background-transition="slide"-->

# Wiki

<div>
위키(wiki)는 불특정 다수가 협업을 통해 <br> **직접 내용과 구조를 수정**할 수 있는 웹사이트를 말한다.
</div><!-- .element: class="fragment fade-up"-->

<div>
일반적인 위키에서 텍스트는 단순화된 <br> **마크업 언어**(위키 마크업)을 이용하여 작성됩니다.
</div><!-- .element: class="fragment fade-up"-->

<div>출처: https://ko.wikipedia.org/wiki/%EC%9C%84%ED%82%A4</div><!-- .element: class="small"-->

---

<!-- .slide: data-background="hsla(0,100%,50%,0.5)" data-background-transition="slide"-->

## 위키 종류

![](https://goo.gl/N9bX9L)

<div>출처: http://www.wikimatrix.org/index.php</div><!-- .element: class="small"-->

---

<!-- .slide: data-background="#757575" data-background-transition="slide"-->

## 위키피디아 & 나무위키

![](https://goo.gl/WDuRZb)<!--.element: class="left"-->

![](https://goo.gl/honhT4)<!--.element: class="right"-->

---

<!-- .slide: data-background="#424242" data-background-transition="slide"-->

## 위키피디아

**원본보기**를 누르면

<div>

![](https://goo.gl/WDuRZb?300)

--

```html
<!-- 머릿글 -->
<div id="mp_header" class="mp_outerbox" style="border:1px solid #a7d7f9; margin: 0 0 0.5em; overflow: hidden; padding: 0.5em; font-size: small; -moz-border-radius: 0.8em; -webkit-border-radius: 0.8em; border-radius:0.8em;">
{| width="100%"
| <div style="float: left; width: 0em; height: 0em; margin: -0.5em 0em 0em -2.5em; overflow: visiable;">[[파일:Wikipedia-logo-v2-200px-transparent.png|140px|링크=]]</div>
<div style="float: left; margin-left:115px"><div style="font-size:1.4em; font-weight: bold">한국어 위키백과에 오신 것을 [[위키백과:환영합니다|환영합니다!]]</div>위키백과는 전 세계 여러 언어로 만들어 나가는 자유 백과사전으로, 누구나 참여하실 수 있습니다.<br/>현재 [[한국어 위키백과]]에는 문서 [[특수기능:통계|'''![](NUMBEROFARTICLES)''']]개가 실려 있습니다.</div>![](-)
|
* ![](Nobr|[[포털:인문학|인문학]])
* ![](Nobr|[[포털:미술|미술]])
* ![](Nobr|[[포털:과학|과학]])
|
* ![](Nobr|[[포털:사회과학|사회과학]])
* ![](Nobr|[[포털:기술|기술]])
* ![](Nobr|'''[[포털:목차/포털|모든 포털]]''')
|}
</div><!-- /머릿글 -->
<!-- 찾기 --><div id="mp_search" class="mp_outerbox" style="border:1px solid #a7d7f9; margin: 0 0 0.5em; background-color: #f9fcff; vertical-align:top; padding:0 0.5em 0 0.5em; overflow: auto; font-size: small; -moz-border-radius: 0.8em; -webkit-border-radius: 0.8em; border-radius: 0.8em;">
{| width="100%"
|<div style="float: left; overflow: hidden;">
<inputbox>
type=search
width=25
buttonlabel=이동
searchbuttonlabel=본문 검색
break=no
</inputbox></div>
```

</div><!-- .element: class="fragment fade-up"-->

---

<!-- .slide: data-background="#616161" data-background-transition="slide"-->

## 나무위키

**편집**을 누르면

![](https://goo.gl/honhT4?300)

--

<div>
{{{#!wiki style="text-align:center"
  '''![]({+2 [[나무위키|{{{#00a495 나무위키)}]]에 오신 것을 환영합니다!}}}'''

나무위키는 누구나 기여할 수 있는 위키입니다.
검증되지 않았거나 편향된 내용이 있을 수 있습니다.
}}}

\---

[include(틀:이용안내)]

\---

[include(틀:나무위키 프로젝트)]

\---

[include(틀:프로젝트 종료, year=2017, month=12, 토론코드=BGdTiba97ubwRXu17fqnE8, time=KST 2017 년 12 월 03 일 23 시 30 분)][include(틀:운영알림)]

\---

[include(틀:운영토론)]

\---

[include(틀:나무위키)]

\---

[[분류:나무위키]]

\## 운영 토론이나 운영 알림은 해당 틀을 편집해 주시기 바랍니다.

</div>

---

<!-- .slide: data-background="#263238" data-background-transition="slide"-->

## 도쿠위키

<div>
![](https://goo.gl/j15V4i)
</div><!-- .element: class="fragment fade-up"-->

---

<!-- .slide: data-background="#263238" data-background-transition="slide"-->

## 원본 보기

![](https://goo.gl/j15V4i?300)

--

```html
====== DokuWiki ======
~~NOTOC~~

DokuWiki(도쿠위키)는 데이터베이스가 필요 없는 사용하기 간단하고 범용성이 높은 오픈 소스 [[wp>ko:위키|위키]] 소프트웨어입니다. 간명하고 읽기 편한 [[wiki:syntax|구문]]으로 사용자에게 사랑을 받고 있습니다. 유지 보수, 백업과 통합이 쉬워 관리자가 선호 합니다. [[:acl|접근 제어 기능]]와 [[:auth|인증에 의한 연결 기능]]을 내장하고 있어, 특히 기업 환경에서의 이용에도 적합합니다. 활기찬 공동체가 기여한 많은 [[:plugins|플러그인]]은 기존의 위키 이외의 광범위한 사용을 가능하게 합니다.

시작하기: [[http://download.dokuwiki.org|![](http://puu.sh/1QA4x.png|최신 버전 다운로드)]]

----

<dokuteaser>
==== 왜 도쿠위키인가? ====
![](:wiki:dokuwiki-128.png?nolink&80)
위키 소프트웨어를 선택할 때 도쿠위키는 인기 있는 선택이고, 유사한 소프트웨어에 비해 많은 장점을 가지고 있습니다.

  * 쉬운 설치와 사용법
  * 낮은 시스템 요구 사항
  * 내장된 접근 제어 목록
  * 다양한 확장 기능
  * 50개가 넘는 언어 지원
  * 디바이스 비의존
  * 오픈 소스

[[:features|도쿠위키 기능에 대해 더 알아보기]]
</dokuteaser>
```

---

<!-- .slide: data-background="#263238" data-background-transition="slide"-->

## 특징

<div>
자료 저장소로 DBMS를 이용하는 대신,<br>
파일 시스템에 평이한 **텍스트 파일로 저장**한다. </div><!-- .element: class="fragment fade-up"-->

<div>
**폴더**를 통해 이름공간 (namespace) 기능을 구현하고 있다.
</div><!-- .element: class="fragment fade-up"-->

<div>
파일 시스템 기반이므로 폴더 째로 복사하면<br>
다른 서버에서 바로 구동할 수 있는 **이동성**을 지닌다. </div><!-- .element: class="fragment fade-up"-->

<div>
**플러그인 시스템**을 지원</div><!-- .element: class="fragment fade-up"-->

---

<!-- .slide: data-background="#263238" data-background-transition="slide"-->

## 어디서 사용할까?

<div>
### 전자정부표준프레임워크 위키페이지

![](https://goo.gl/uYLLFG)
![](https://goo.gl/rKw22S)

</div><!-- .element: class="fragment fade-up"-->

---

<!-- .slide: data-background="#827717" data-background-transition="slide"-->

### Clojure Korea Wiki

![](https://goo.gl/g6YLj8)

---

<!-- .slide: data-background="green" data-background-transition="slide"-->

## 그리고

<div>
# 지금 보고 있는
# 이 슬라이드!!

**revealjs**를 사용하여 만들었습니다.

</div><!-- .element: class="fragment fade-up"-->

---

<!-- .slide: data-background="#4E342E" data-background-transition="slide"-->

# 감사합니다.

![](https://goo.gl/LDteHk?.png)
