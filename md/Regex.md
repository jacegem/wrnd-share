---
customTheme : "my-theme"
theme : "night"
transition: "slide"
transitionSpeed: 'slow'
highlightTheme: "darkula"
---

<!-- .slide: data-background="https://goo.gl/oNpyLA" class="dark"-->

# 정규표현식

## 정규표현식의 사전적인 의미<!-- .element: class="fragment fade-up block"-->

<div>
특정한 규칙을 가진<br>
**문자열의 집합**을 표현하는데 사용하는<br>
**형식 언어**</div><!-- .element: class="fragment fade-up block orange"-->

---

<!-- .slide: data-background="https://goo.gl/R1cQZo" data-background-transition="zoom" -->

## 정규표현식 사용해보기

```python
# 따옴표(')로 둘러쌓인 부분에 원하는 정규표현식을 적습니다.

regex = r'0\d{1,2}[ -]?\d{3,4}[ -]?\d{3,4}' # 전화번호를 찾는 정규표현식

# 주소록입니다. 이후 강의에서 모두 이 search_target 을 사용합니다.

search_target = '''Luke Skywarker 02-123-4567 luke@daum.net
다스베이더 070-9999-9999 darth_vader@gmail.com
princess leia 010 2454 3457 leia@gmail.com'''

# 정규표현식과 일치하는 부분을 모두 찾아주는 파이썬 코드입니다.

import re
result = re.findall(regex, search_target)
print("\n".join(result))
```

<!-- .element: class="fragment fade-up"-->

<div>
결과
```python
02-123-4567
070-9999-9999
010 2454 3457
```
</div>
<!-- .element: class="fragment fade-up"-->

<div>출처: https://programmers.co.kr/learn/courses/11</div><!-- .element: class="small"-->

--

<!-- .slide: data-background="https://goo.gl/diUgLg" data-background-transition="zoom" -->

# http://repl.it/

실습은 이곳에서 진행합니다.

<div>
> REPL : Read-Eval-Print Loop의 약자로 스칼라, 파이썬 등 대화형 환경
>
> 콘솔에서 컴파일 없이 코드를 입력하고 출력 결과를 확인 할 수 있는 환경
</div>
<!-- .element: class="fragment fade-up"-->

--

<!-- .slide: data-background="https://goo.gl/diUgLg" data-background-transition="zoom" -->

**Python3**을 선택합니다.

![](https://goo.gl/vWhg5j)

<div>
실행화면
![](https://goo.gl/4XLb32)
</div><!-- .element: class="fragment fade-up"-->

---

<!-- .slide: data-background="https://goo.gl/c5DKSv" data-background-transition="zoom" -->

## 구성요소

- 메타 문자
- 이스케이프 문자
- 특수 문자
- 괄호 (대괄호, 중괄호, 소괄호)

--

<!-- .slide: data-background="https://goo.gl/qdF1iK" data-background-transition="slide" -->

## 메타 문자

<span class="fragment highlight-current-red">. (dot)</span>
<span class="fragment highlight"> : 숫자와 문자 특수기호, 공백 등을 포괄한 **모든 범위의 한 글자** ![](https://goo.gl/SotRqm)</span>

<span class="fragment highlight-current-red">^ (circumflex)</span>
<span class="fragment highlight"> : 문자열의 시작점. 그러나 일반적으로는 **한 줄의 시작점**을 의미한다. 문자클래스 집합에서는 다른 의미를 갖는다.![](https://goo.gl/mcyQB7)</span>

<span class="fragment highlight-current-red">$ (dollar)</span>
<span class="fragment highlight"> : 문자열의 끝점. 그러나 일반적으로는 **한 줄의 끝점**을 의미한다. ![](https://goo.gl/UegnzB)</span>

<span class="fragment highlight-current-red">\ (back slash)</span>
<span class="fragment highlight"> : 메타문자를 검색하기 위하여 특수문자 앞에 사용한다. 마침표 `.` 를 찾기 위해 `\.` 을 사용한다.</span>

<span class="fragment highlight-current-red">| (vertical bar)</span>
<span class="fragment highlight"> : '**또는**'을 의미한다. (고구려|백제|신라) 를 찾으면 고구려 또는 백제, 신라를 찾게 된다.</span>

--

<!-- .slide: data-background="https://goo.gl/EUwNxG" data-background-transition="slide" -->

## 이스케이프 문자

<span class="fragment highlight-current-red">`\w`</span>
<span class="fragment highlight"> : 영문자와 숫자, 언더스코어(\_) ![](https://goo.gl/dgkxYA)</span>

<span class="fragment highlight-current-red">`\W`</span>
<span class="fragment highlight"> : 영문자와 숫자, 언더스코어(\_)가 아닌 문자 ![](https://goo.gl/ZMfpWx)</span>

<span class="fragment highlight-current-red">`\d`</span>
<span class="fragment highlight"> : 10 진수로 된 숫자 ![](https://goo.gl/1Sj781)</span>

<span class="fragment highlight-current-red">`\D`</span>
<span class="fragment highlight"> : 10 진수 숫자 가 아닌 모든 문자(공백 포함) ![](https://goo.gl/o3X3Fe)</span>

<span class="fragment highlight-current-red">`\s`</span>
<span class="fragment highlight"> : 탭, 줄바꿈 등 지정된 공백문자[\t\n\r\f\v] ![](https://goo.gl/RV8cac)</span>

<span class="fragment highlight-current-red">`\S`</span>
<span class="fragment highlight"> : 위 공백문자가 아닌 모든 글자 ![](https://goo.gl/N7SHTb)</span>

<span class="fragment highlight-current-red">`\t`</span>
<span class="fragment highlight"> : 일반적으로 탭(TAB) 키를 입력했을 때 나오는 일정 간격을 유지하는 공백 ![](https://goo.gl/YcDejH)</span>

---

<!-- .slide: data-background="https://goo.gl/EUwNxG" data-background-transition="slide" -->

## 글자 대표문자 \w

<div>

```python
# 따옴표(')로 둘러쌓인 부분에 원하는 정규표현식을 적습니다.
regex = r'\w'

search_target = '''Luke Skywarker 02-123-4567 luke@daum.net
다스베이더 070-9999-9999 darth_vader@gmail.com
princess leia 010 2454 3457 leia@gmail.com'''

# 정규표현식과 일치하는 부분을 모두 찾아주는 파이썬 코드입니다.

import re
result = re.findall(regex, search_target)
print("\n".join(result))
```

</div>
<!-- .element: class="fragment fade-up"-->

<div>
결과

```python
L
u
k
e
S
k
y
w
a
r
k
e
r
0
2
1
2
.. 이하 생략 ..
```

</div><!-- .element: class="fragment fade-up"-->

---

<!-- .slide: data-background="https://goo.gl/EUwNxG" data-background-transition="slide" -->

## 숫자 대표문자 \d

<div>

```python
# 따옴표(')로 둘러쌓인 부분에 원하는 정규표현식을 적습니다.
regex = r'\d'

# 주소록입니다. 이후 강의에서 모두 이 search_target 을 사용합니다.

search_target = '''Luke Skywarker 02-123-4567 luke@daum.net
다스베이더 070-9999-9999 darth_vader@gmail.com
princess leia 010 2454 3457 leia@gmail.com'''

# 정규표현식과 일치하는 부분을 모두 찾아주는 파이썬 코드입니다.

import re
result = re.findall(regex, search_target)
print("\n".join(result))
```

</div><!-- .element: class="fragment fade-up"-->

<div>

결과

```python
0
2
1
2
3
4
5
6
7
0
7
0
9
9
9
9
9
.. 이하 생략 ..
```

</div><!-- .element: class="fragment fade-up"-->

---

<!-- .slide: data-background="https://goo.gl/EUwNxG" data-background-transition="slide" -->

## 특수 문자

<span class="fragment highlight-current-red">?</span>
<span class="fragment highlight"> : 문자가 없거나 하나인 경우 ![](https://goo.gl/SotRqm)</span>

<span class="fragment highlight-current-red">\*</span>
<span class="fragment highlight"> : 문자가 없거나 하나 이상 존재하는 경우 ![](https://goo.gl/SotRqm)</span>

<span class="fragment highlight-current-red">+</span>
<span class="fragment highlight"> : 문자가 하나 이상 존재하는 경우 ![](https://goo.gl/SotRqm)</span>

---

<!-- .slide: data-background="https://goo.gl/EUwNxG" data-background-transition="slide" -->

## 하나 이상

+<!-- .element: class="fragment grow"-->

<div>

```python
#regex에는 넣는 값 중, 따옴표(')로 둘러쌓인 부분에 원하는 정규표현식을 적습니다.
regex = r'\d+'

search_target = '''Luke Skywarker 02-123-4567 luke@daum.net
다스베이더 070-9999-9999 darth_vader@gmail.com
princess leia 010 2454 3457 leia@gmail.com'''

import re
result=re.findall(regex,search_target)
print(result)
```

</div><!-- .element: class="fragment fade-up"-->

<div>

결과

```python
['02', '123', '4567', '070', '9999', '9999', '010', '2454', '3457']
```

</div><!-- .element: class="fragment fade-up"-->

---

<!-- .slide: data-background="https://goo.gl/EUwNxG" data-background-transition="slide" -->

## 대괄호: 문자 클래스의 집합

> 문자 클래스란 문자열, 특수문자 등을 등장할 수 있는 형태를 표시한 것

<span class="fragment highlight-current-red">`[0-9]`</span>
<span class="fragment highlight"> : 0 부터 9 까지의 숫자 집합을 의미 ![](https://goo.gl/Lgcker)</span>

<span class="fragment highlight-current-red">`[A-Z]`</span>
<span class="fragment highlight"> : 영어 대문자 집합 ![](https://goo.gl/x9etG3)</span>

<span class="fragment highlight-current-red">`[AEIOUaeiou]`</span>
<span class="fragment highlight"> : 영어에서 a, e, i, o, u 로 이루어진 대소문자 집합 ![](https://goo.gl/9773v3)</span>

<span class="fragment highlight-current-red">`[가-힣]`</span>
<span class="fragment highlight"> : 가부터 힣까지의, 한글자모부분을 제외한 한글 집합 ![](https://goo.gl/9dR2DL)</span>

---

<!-- .slide: data-background="https://goo.gl/EUwNxG" data-background-transition="slide" -->

## 대괄호: 문자 클래스의 집합

> 대괄호 내에 ^가 들어가면 ^ 뒤에 나오는 문자 클래스는 해당 집합에서 제외한다는 의미

<span class="fragment highlight-current-red">`[^0-9]`</span>
<span class="fragment highlight"> : 0 부터 9 까지의 숫자 집합을 제외한다는 의미이며, 이스케이프 문자 \D 와 동일한 의미 ![](https://goo.gl/UQT5CN)</span>

<span class="fragment highlight-current-red">`^[^A-Z]`</span>
<span class="fragment highlight"> : 행의 앞쪽이 영어 대문자 집합인 것을 제외하고 찾으라는 의미 ![](https://goo.gl/8gLbnp)</span>

<span class="fragment highlight-current-red">`[0-9+\-*/\^\(\)=]`</span>
<span class="fragment highlight"> : 숫자와 사칙연산 부호 등(+, -, \*, /, ^, \=\)을 찾으라는 의미 ![](https://goo.gl/He9CmC)</span>

---

<!-- .slide: data-background="https://goo.gl/EUwNxG" data-background-transition="slide" -->

## 중괄호: 수량자

> 수량자 앞의 글자 혹은 문자클래스 집합의 글자수가 얼마나 되는지를 지정하는 것

<span class="fragment highlight-current-red">`[0-9]{5}`</span>
<span class="fragment highlight"> : 5 자리의 숫자 집합 ![](https://goo.gl/3mgKjK)</span>

<span class="fragment highlight-current-red">`[A-Za-z]{3,}`</span>
<span class="fragment highlight"> : 3 글자 이상의 영어 단어 집합 ![](https://goo.gl/HD6pCt)</span>

<span class="fragment highlight-current-red">`[A-Za-z0-9]{4,8}`</span>
<span class="fragment highlight"> : 4 글자 이상 8 글자 이하의 영어 대소문자와 숫자로 이루어진 집합 ![](https://goo.gl/kNseMp)</span>

---

<!-- .slide: data-background="https://goo.gl/EUwNxG" data-background-transition="slide" -->

## 수량자 & 특수문자

| 특수문자 | 대응수량자 | 설명                    |
|------|-------|-----------------------|
| ?    | {0,1} | 문자가 없거나 하나인 경우        |
| \*   | {0,}  | 문자가 없거나 하나 이상 존재하는 경우 |
| +    | {1,}  | 문자가 하나 이상 존재하는 경우     |

---

<!-- .slide: data-background="https://goo.gl/EUwNxG" data-background-transition="slide" -->

## 게으른 수량자 ?

<span class="fragment highlight-current-red">`.+`</span>
<span class="fragment highlight"> : 한 줄을 의미 ![](https://goo.gl/wMvgME)</span>

<span class="fragment highlight-current-red">`.+?`</span>
<span class="fragment highlight"> : \.와 동일한 결과를 가져온다. ![](https://goo.gl/v7mkiC)</span>

<span class="fragment highlight-current-red">`.{3,}`</span>
<span class="fragment highlight"> : 3 글자 이상의 한 줄 ![](https://goo.gl/YDbi8F)</span>

<span class="fragment highlight-current-red">`.{3,}?`</span>
<span class="fragment highlight"> : 한 줄을 3 글자 단위로 끊은 결과를 보여준다. ![](https://goo.gl/WJPUJD)</span>

---

<!-- .slide: data-background="https://goo.gl/EUwNxG" data-background-transition="slide" -->

## 소괄호: 그룹

<div>

예제문단
```
충청남도를 충청남도라고 한다. 옳다.
충청북도를 충청남도라고 한다. 잘못되었다.
충청도를 충청남도라고 한다. 역시 잘못되었다.
```
</div><!-- .element: class="fragment fade-up"-->

<span class="fragment highlight-current-red">`충청(남|북)?도`</span>
<span class="fragment highlight"> : 충청남도, 충청북도, 충청도를 의미 ![](https://goo.gl/xHvxbG)</span>

<span class="fragment highlight-current-red">`(충청(남|북)?도)를 \1`</span>
<span class="fragment highlight"> : 위에서 찾은 단어들을 하위 표현식으로 묶어서 역참조에 활용한 것이다. 이 경우 **첫째 줄부분**만이 검색된다. ![](https://goo.gl/R2Qet4)</span>

<div>출처: https://librewiki.net/wiki/정규표현식</div><!-- .element: class="small" -->

---

<!-- .slide: data-background="https://goo.gl/EUwNxG" data-background-transition="slide" -->

## 사용예시 URL

<div>

문자열에서 **URL**을 찾는 정규표현식의 예제
```python
(http|https|ftp|telnet|news|mms)://[^\"'\s()]+
```
</div><!-- .element: class="fragment fade-up"-->

<div>
### (http|https|ftp|telnet|news|mms)://[^\"'\s()]+
</div><!-- .element: class="fragment fade-up"-->

---

<!-- .slide: data-background="https://goo.gl/EUwNxG" data-background-transition="slide" -->

## 사용예시 - 이메일

<div>

웹사이트의 회원가입절차에서 이메일 주소 폼에 **이메일**을 제대로 입력했는지 검증
```python
^[0-9a-zA-Z]([\-.\w]*[0-9a-zA-Z\-_+])*@([0-9a-zA-Z][\-\w]*[0-9a-zA-Z]\.)+[a-zA-Z]{2,9}$
```
</div><!-- .element: class="fragment fade-up"-->

<div>

### ^[0-9a-zA-Z]([\-.\w]*[0-9a-zA-Z\-_+])*@([0-9a-zA-Z][\-\w]*[0-9a-zA-Z]\.)+[a-zA-Z]{2,9}$

![](https://goo.gl/86poyd)

</div><!-- .element: class="fragment fade-up"-->

---

<!-- .slide: data-background="https://i.ytimg.com/vi/9HMzwFl5OLY/maxresdefault.jpg" data-background-transition="zoom" -->

# 감사합니다.

> (들어주셔서)?\s(정말)+\s((감사|사랑)합|고맙습)니다.?

![](https://goo.gl/uBb5gj)

---

<!-- .slide: data-background="https://goo.gl/EUwNxG" data-background-transition="slide" -->

출처

- https://librewiki.net/wiki/정규표현식
- http://www.nextree.co.kr/p4327/
- https://regexper.com
- https://programmers.co.kr/learn/courses/11/

연락처

- 이메일: **jykwon@wavus.co.kr**
