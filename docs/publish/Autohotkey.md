---
customTheme : "my-theme"
theme : "night"
transition: "slide"
transitionSpeed: 'slow'
highlightTheme: "darkula"
---

<!-- .slide: data-background="https://goo.gl/1aLJ4d" data-background-transition="slide" -->

<div>
## 안녕하세요.
</div><!-- .element: class="fragment fade-up"-->

--

<!-- .slide: data-background="https://goo.gl/igMrwa" data-background-transition="slide" -->

<div>
![](https://goo.gl/PffXTZ?.png)
</div><!-- .element: class="fragment fade-up"-->

---

<!-- .slide: data-background="https://goo.gl/w4a9XA" data-background-transition="slide" -->

## 순위 어디에도 없는 언어

<div>
**AutoHotKey** 에 대해 이야기 해보려 합니다.
</div><!-- .element: class="fragment fade-up"-->

---

<!-- .slide: data-background="https://goo.gl/UfMdw8" data-background-transition="slide" -->

# AutoHotKey

<div>
오토핫키(AutoHotkey)는 <br> **윈도우** 응용 프로그램 및 매크로를 만드는 <br> **오픈 소스** 자유 소프트웨어이다. </div><!-- .element: class="fragment fade-up"-->

<div>
사용자가 **반복작업을 자동**으로 할 수 있도록 도와준다. </div><!-- .element: class="fragment fade-up"-->

<div>
**단축키**를 제공하기 위한 스크립트 언어로 제공된다.

<div>출처: https://ko.wikipedia.org/wiki/오토핫키</div><!-- .element: class="small"-->

</div><!-- .element: class="fragment fade-up"-->

---

<!-- .slide: data-background="https://goo.gl/RBHja9" data-background-transition="slide" -->

## 관련 사이트

<div>

- 홈페이지 : https://autohotkey.com/
- AutoHotKey 포럼 : http://www.autohotkey.co.kr/
- GitHub : https://github.com/Lexikos/AutoHotkey_L
  </div><!-- .element: class="fragment fade-up"-->

---

<!-- .slide: data-background="https://goo.gl/SMLsLc" data-background-transition="slide" -->

## 사용하게 된 이유

<div>
키보드를 바꾸고 싶었죠.
![](https://goo.gl/Gs8inp)
</div><!-- .element: class="fragment fade-up"-->

<div>
당황스럽게 fn키, 방향키가 없고, Control키의 위치가 다릅니다.
![](https://goo.gl/bpaXMf)
</div><!-- .element: class="fragment fade-up"-->

<div>
이 키보드에 적응할 수 있을지 테스트 하기위해 <br> **autohotkey**를 사용하였습니다.
</div><!-- .element: class="fragment fade-up"-->

---

<!-- .slide: data-background="https://goo.gl/FfpgbE" data-background-transition="slide" -->

## 몇 가지 기호들

| 기호    | 설명        |
|-------|-----------|
| **#** | 윈도우 키     |
| **!** | Alt 키     |
| **^** | Control 키 |
| **+** | Shift 키   |

그 외에... 등등등..

---

<!-- .slide: data-background="https://goo.gl/7mJGQ5" data-background-transition="slide" -->

## 간단한 예제

```autohotkey
#n::Run Notepad
```

<div>
스크립트를 실행하면 트레이 아이콘이 생겨요
![](https://goo.gl/v45wmC)
</div><!-- .element: class="fragment fade-up"-->

<div>
윈도우 + n 키를 누르면 메모장이 실행되요
![](https://goo.gl/CEtAon)
</div><!-- .element: class="fragment fade-up"-->

--

<!-- .slide: data-background="https://goo.gl/psMdPs" data-background-transition="zoom" -->


## 간단한 예제 2

```autohotkey
^!s::
Send Sincerely,{enter}John Smith  ; This line sends keystrokes to the active (foremost) window.
return
```

<div>
Ctrl + Alt + s 를 누르면 <br>
내용이 **자동**으로 입력됩니다.

![](https://goo.gl/LY6akr)

</div><!-- .element: class="fragment fade-up"-->

---

<!-- .slide: data-background="https://goo.gl/FtYsDB" data-background-transition="slide" -->

## 현재 사용하고 있는 것들

### HotKeys

| 입력 키               | 맵핑 키               |
|--------------------|--------------------|
| Capslock + a,s,d,f | Ctrl + a,s,d,f     |
| Capslock + i,k,j,l | Ctrl + i,k,j,l     |
| Capslock + 1,2,3,4 | Fn1, Fn2, Fn3, Fn4 |

---

<!-- .slide: data-background="https://goo.gl/FtYsDB" data-background-transition="slide" -->

### HotStrings

```autohotkey
:*:%%%::
	Send, %A_YYYY%년 %A_MM%월 %A_DD%일 %A_HOUR%시 %A_MIN%분
	Return
:*:$$::
	Send, %A_YYYY%.%A_MM%.%A_DD%
	Return
:*:/bg::
	Set_Absolutely_English("bg-zoom slide slow ---->")
	return
:*:/nw::
	Set_Absolutely_English("<nowiki></nowiki>")
	Send {LEFT 9}
	return
```

---

<!-- .slide: data-background="https://goo.gl/FtYsDB" data-background-transition="slide" -->

### 특정 프로그램에서 동작

```autohotkey
#ifWinActive ahk_exe Xshell.exe

;<<Short Cut>>
CapsLock & c::Send ^{INSERT}	;; copy
CapsLock & v::Send +{INSERT}	;; paste
CapsLock & j:: Send ^+{TAB}
CapsLock & l:: Send ^{TAB}
CapsLock & x::Send ^c 		;; send break signal to terminal

^c::Send ^{INSERT}	;; copy
^v::Send +{INSERT}	;; paste
^x::Send ^c 		;; send break signal to terminal
^+x::Send ^{BS}         ;; send break signal to SunOS system
^n::Send +!n

#ifWinActive
```

---

<!-- .slide: data-background="https://goo.gl/A6NUqQ" data-background-transition="slide" -->

## GUI

<div>
간단한 코드로 GUI 프로그램도 만들수 있습니다.

```autohotkey
Gui, add, text, y+10 Section, ID:
Gui, add, text, xs y+12, Password:
Gui, add, edit, vid ys Section ; The ym option starts a new column of controls.
Gui, add, edit, vpw xs Password
Gui, add, button, default ys Section gSave, Save  ; The label ButtonOK (if it exists) will be run when the button is pressed.
Gui, add, button, default ys gHelp, Help
Gui, add, button, default xs Section gRun, Run  ; The label ButtonOK (if it exists) will be run when the button is pressed.
Gui, Add, DDL, vhour w50 xm Section, 00|01|02|03|04|05|06|07|08||09|10|11|12|13|14|15|16|17|18|19|20|21|22|23|24
Gui, add, text, ys , H
Gui, add, button, default ys gSetSchedule, Set Schedule
Gui, add, button, default ys gDeleteSchedule, Delete Schedule
Gui, add, button, default ys gClose, Close
Gui, show,, Get Free E-Book
```

![](https://goo.gl/wHiXZu)

</div><!-- .element: class="fragment fade-up"-->

---

## Autohotkey 실습

쿠키 클리커 게임

![](https://goo.gl/hZ4a7A)

http://orteil.dashnet.org/cookieclicker/

--

## 스크립트

```autohotkey
capslock & 0::
	mode = 0
	return

; 화면 왼쪽의 쿠키를 클릭한다.
capslock & 1::
  mode = 1
  Loop,
  {
    if (mode = 0){
      return
    }
    else if (mode = 1){
      MouseClick, left, 222, 533, 1
    }
  }
  return
```

---

<!-- .slide: data-background="https://goo.gl/4MPQuh" data-background-transition="slide" -->

## 감사합니다.

<div>
더 자세한 내용은 https://autohotkey.com/docs/AutoHotkey.htm 을 참조하시기 바랍니다.

![](https://goo.gl/dwTx8Z)

</div><!-- .element: class="fragment fade-up"-->
