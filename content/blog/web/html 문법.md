---
title: html
date: "2022-07-12T22:12:03.284Z"
description: ""
---


### vscode setting

- Live Server 를 통해서 HTML 코드를 실행(실시간)
- View in Browser
- Beautify (ctrl+shif+l)
- Auto Rename Tag
- html tag wrapper (ctrl+i)
- prettier
- eslint
- path intellisense
- Bracket Pair Colorizer
- Material Icon Theme

기본브라우저 설정 =>  제어판>프로그램>기본 프로그램>기본앱>웹 브라우저 Microsoft edge를 Chrome으로 변경

### 웹의 기본 특성

- 모든 경로의 폴더/파일명
- 영문(대소구분)
- 숫자
- _ - 사용
- 꼭 첫글자는 영문(숫자 안됨)
- 모든 html(태그,요소,element)는 영문 소문자
- 선 저장! 후 테스트!(끌어다 쓰는 파일 때문에)
- 해당 에디터 - root 정해 놓고 작업 시작
- html은 거의 , 대부분 시작태그<태그명>와 끝태그</태그명>로 구성되어있다. 예외 - <meta>,
- 폰트의 기본 css(글꼴:굴림, 크기:14px, 색상:#0000)

### 웹문서의 종류

- .html(웹문서), .php, .asp, .jsp …
- .css
- .js
- .xml, .json …

# .html

젠코딩

```html
!
```

## 주언어 명시

<**html lang="ko" xml:lang="ko"** xmlns="[http://www.w3.org/1999/xhtml](http://www.w3.org/1999/xhtml)"> xhtml 계열일경우

<html lang="ko"> 그외 5,4

주언어 명시는 콘텐츠가 있을 때 필요한 것이므로, 내용이 없는 빈 프레임의 경우 선언하지 않아도 오류 아님

영어는 <html lang="en">

독일어는 <html lang="de">

일어는 <html lang="ja">

중국어는 <html lang="zh">

프랑스어는 <span lang="fr">

대부분 태그는 body의 자식들

head는 화면에 표시되지 않는 미리 처리되어야할 것들

## 문자 코드 세팅(콘텐츠 타입 선언)

- 영어 이외의 모든 언어는 계산해야 구현가능

```jsx
<meta charset="UTF-8">
```

지금은 전부 UTF-8 로 통일되었음(유니코드)

<title>브라우저 탭에 표시되는 웹페이지의 제목</title>

>> 세부페이지도 세부적으로

## 태그의 종류와 특징

```jsx
<p></p>
// 단락(기본css - margin 있음) 

```

## css 스타일링 3가지 방식

css속성:값;css속성:값;css속성:값;

### 로컬스타일, 인라인스타일(안 씀..)

태그에 직접 쓰는 방법
style 확장 태그를 주어 사용하는 방식(비효율적, **안 씀!!**)

```html
<p style="font-size:16px; font-weight:bold; color:red; ">
```

### 임베디드 스타일, 페이지 스타일(기본 스타일 적용)

XHTML 문서에 스타일을 포함하는 방법

```html
<head></head> 태그 사이에 코딩
```

```html
<style type="text/css">
h1 {font-size: 16px;}
p {color:red;}
</style>
```

### 링크드 스타일(가장 적합!)

분리되어 있는 **css파일**을 링크하는 방법=>가장 적합한 방법(코드 **중복**을 줄일 수 있음)

```html
<head></head> 태그 사이에 코딩
```

```html
// 닫는 태그 없음
<link /> // 이런 방식

<link href="css파일의 경로" media="screen" rel="stylesheet" type="text/css" />
```

젠코딩

```html
link
```

### css 경로

css폴더(친구레벨)

친구레벨 표시방법(생략 가능)

```html
./
```

경로 예시 

```html
./css/ex.css
```

### css파일 작성

```css
p{font-size: 30px;
    font-weight: bold;
    font-family: '돋움';
    color: red;
    background: green;
}
```

## 우선 순위

### 인라인 방식 > 임베디드 방식 > 링크드 방식

*(인라인과 임베디드 충돌하면 인라인 적용)*

어떤 속성이 충돌되면 이기는 속성(최종적으로 마지막의 계산되는) 

계산 순서는 우선순위 낮은것부터 높은 것이 뒤에 **덮여 적용되는 방식**

- 우선 순위 개념은 다른 코드에서도 적용됨

![Untitled](html%2022%2006%2024-%2064b543fc25ac4aa382ce769045ab403b/Untitled.png)


## 주석

실제 브라우저가 계산하지 않는 코드

html,css 주석 젠코딩

- 드래그 **ctr + /**
- 맥 **command + /**

html 주석

```html
<!-- -->
```

css 주석

```css
/* */
```

# 헤드라인(제목→목차outline) 태그

```html
<h1></h1>
...
<h6></h6>

```

```html
<!DOCTYPE html>
<html lang="ko">
    <head>
        <meta charset="UTF-8">
        
        <title>Document</title>
        <link rel="stylesheet" href="./css/ex.css">
        <style>

        </style>
    </head>
    <body>
        <h1>제목요소입니다</h1>
        <h2>제목요소입니다</h2>
        <h3>제목요소입니다</h3>
        <h4>제목요소입니다</h4>
        <h5>제목요소입니다</h5>
        <h6>제목요소입니다</h6>

        

    </body>
</html>
```

### h(Head)태그 기본 css

크롬에서 선택 후 - 검사

```css
h1 {
    display: block;
    font-size: 2em;
    margin-block-start: 0.67em;
    margin-block-end: 0.67em;
    margin-inline-start: 0px;
    margin-inline-end: 0px;
    font-weight: bold;
}
```

### h 태그 - 접근성

>>> 목차

- xhtml에서는 목차를 주는 태그는 이것 하나 뿐
- 하나의 html 페이지에는 **꼭!!!! 1개의 <h1>태그**가 존재한다!!!
- **h1 - 사이트의 로고**
- 상속시(css) 폰트사이즈는 영향을 받지 않는다.(다시체크)

### 크롬 익스텐션 “HTML5 Outliner”

![Untitled](html%2022%2006%2024-%2064b543fc25ac4aa382ce769045ab403b/Untitled%201.png)

- 헤딩 번호를 정하는 것은 사이즈가 되면 안 된다.
- 헤딩은 목차 개념으로 접근할 것
- 번호 건너뛰기 금지

- 스크린 리더기가 h1~6을 구분해서 읽어준다(ex “헤딩1”)

## div 태그

- 빈 박스 - 레이아웃을 구성하는 주 태그(xhtml에서는 유일)
- margin없음
- 한줄 차지

![Untitled](html%2022%2006%2024-%2064b543fc25ac4aa382ce769045ab403b/Untitled%202.png)

박스 사이즈 조정

width: 000px; height: 000px

## span, strong, em 태그

```html
<span>웹표준</span>과 <strong>접근성</strong>을 <em>준수</em>합시다.
```

![Untitled](html%2022%2006%2024-%2064b543fc25ac4aa382ce769045ab403b/Untitled%203.png)

- 특정 단어에 시각적 표현이나 강조를 하기 위한 태그

**span** - 기본 값은 없으나, css로 표현할 수 있음(주관적 표현)

**strong** - font-weight: bold; (강한 강조)

**em** - font-style: italic; (약한 강조)

“시각적 표현을 넘어 접근성을 위해 구분”

```html
<p><span>웹표준</span>과 <strong>접근성</strong>을 <em>준수</em>합시다.</p> 
<p><span>웹표준</span>과 <strong>접근성</strong>을 <em>준수</em>합시다.</p> 
<p><span>웹표준</span>과 <strong>접근성</strong>을 <em>준수</em>합시다.</p> 
        
<span>웹표준</span>
<span>웹표준</span>
<span>웹표준</span>
<span>웹표준</span>
```

![Untitled](html%2022%2006%2024-%2064b543fc25ac4aa382ce769045ab403b/Untitled%204.png)

## br 태그

줄바꿈, 끝태그 없음

## 스페이스바 역할(쓰지마 걍)

```html
&nbsp;
```

## ©카피라이터(특수문자쓰지말고 이걸로)

```html
&copy;
```

## 주의할 특수 문자(그냥 치면 에러 생길 수 있음)

```html
// <>
&lt;
&gt;

// &
&amp;
```

엔티티 정리 사이트(유니코드 쓰기)

[HTML 엔티티](https://unicode-table.com/kr/html-entities/)

## display: block;


# 태그의 분류

![Untitled](html%2022%2006%2024-%2064b543fc25ac4aa382ce769045ab403b/Untitled%205.png)

## block-level Element

- <h1>~<h6><p><div> (<html><body>),dl dt dd
- 수직 정렬
- width 부모 태그의 폭에 100%
- block 요소는 inline요소의 부모 계층으로만 사용할 수 있다.
- 종속 관계 - html>body>div>h,p

## inline-level Element

- <span><strong><em><abbr><acronym><del><ins>
- 수평 정렬
- width 콘텐츠 요소의 길이/양에 맞춰
- inline요소는 block요소의 자식 계층으로만 사용할 수 있다.
- inline요소들 간 서로 종속할 수 있다(예외:  ).

<aside>
💡 종속 관계를 지키지 않아도 에러가 나지 않는다. 틀린 문법은 접근성에 걸리게 된다.

</aside>

22.06.30(목)

# <a> 태그

- inline tag

```html
<a href="https://naver.com" title="네이버로이동합니다">네이버로이동</a>
```

- 태그 속성 title은 마우스오버에 툴팁표시가 됨
- 접근성!! - **스크린 리더기가 title을 읽음(링크에 글도 읽어줌- 이경우 두 번 네이버라고 두 번 알려준 코드)**

href=”페이지주소”

### target=”_blank” 새 창(탭)으로 열기(_self는 기본)

```html
<a href="https://naver.com" title="네이버로이동합니다" target="_blank">네이버로이동</a>
```

### 접근성 **_blank**의 사용 규칙

- 다른 사이트, 제휴 사이트
- **title** 속성과 꼭 함께 사용해야한다.(리더기를 통해서는 갑자기 다른 사이트부터 읽어버리기 때문에) - “새 창의 열림” 식으로 표현도 가능

### 내부 링크

```html
<a href="./sub1.html">회사소개</a>
```

### 상속시(css)

text-decoration/color 는 영향받지 않는다(기본 - blue, purple)

### 가상 클래스의 앵커(a) 링크

**link** - 최초 페이지가 열렸을때 상황(기본)
**visited** - 사용자가 과거에 링크를 선택한 적이 있을때
**hover** - 현재 마우스 포인터 등으로 가리켜지고 있을때(롤오버)  ****

<aside>
💡 ***호버만큼은 모든 태그에 사용할 수 있다***

</aside>

**active** - 현재 클릭되고 있을때(클릭 상태 유지)

**focus** - 포커스를 받을 때 (점선, 박스 등으로 포커스 표시)

```css
.link a:link{text-decoration: none; color: red;} 
//:link는 안 써도 기본
.link a:visited{text-decoration: none;color: green;}
.link a:hover{text-decoration: underline;color: orange;}
.link a:active{text-decoration: none;color: pink;}
.link a:focus{text-decoration: underline;color: blue;}
```

```html
<!DOCTYPE html>
<html lang="ko">
    <head>
        <meta charset="UTF-8">
        <title>Document</title>
        <style>
            .link .link1{text-decoration: none; color: red;}
            .link .link1:hover{text-decoration: underline;color: orange;}

            .link .link2{text-decoration: none; color: yellow;}
            .link .link2:hover{text-decoration: underline;color: green;}
         </style>
    </head>
    <body>

        <div class="link">
            <a class="link1" href="https://naver.com" title="네이버로이동합니다" target="_blank">네이버로이동</a>
            <a class="link1" href="https://daum.net" target="_self">다음으로이동</a>
            <a class="link1" href="https://google.com">구글로이동</a>
            <a class="link2" href="./sub1.html">회사소개</a>
            <a class="link2" href="https://nate.com">네이트로 이동</a>
        </div>
        
    </body>
</html>
```

### 속성으로 지정

```css
.link a[title]{color: red;}
/* title로 지정 */

.link a[title="네이버"]{color: red;}
/* title이 네이버인 것을 지정 */

.link a[href^="https://daum"]{color: red;}
/* 유사 콘텐츠 지정 */
/* ^는 앞을 의미, daum으로 시작하는 사이트 */

.link a[href$="https://.com"]{color: red;}
/* $는 뒤, .com이 포함된 것을 지정 */

```

### 응용

```css
.link .link1:hover{text-decoration: underline;color: orange;}
```

### 파일 링크

```html
<a href="./images/a1.jpg">이미지파일</a>
<a href="./images/text.txt">텍스트파일</a>
```

### 임시 링크

```html
<a href="#">
```

>> #id_name으로 부를 수 있음

### 다운로드 링크

- 웹 브라우저가 처리할 수 없는 파일의 종류를 href=”” 로 연결할 때

```html
<a href="./images/text.zip">다운로드</a>
```

- download 속성 부여방식

```html
<a href="./images/text.txt" download="./images/text.txt">다운로드</a>
```

### 젠코딩 - 여러 개 만들기

```html
p*300{$$단락입니다}
a*2

// 만들 태그 뒤에 곱하기 표시로 작동
```

### 점프 메뉴

- 한 페이지 안에서 이동

```html
<a href="#new">신제품 소개로 이동</a>
<a href="#best">인기상품 베스트 50으로 이동</a>

<h3 id="new">신제품 소개</h3>
<h3 id="best">인기상품 베스트 50</h3>

<a href="#top">Top</a>
```

# ul, ol, dl 목록 태그

## ul

- 순서없는 목록(unorder list)
- li 블릿
- 직계 자식은 **꼭!!! <li>만** 올 수 있다.

<aside>
💡 문법 지키자!

</aside>

```html
<ul>
	<li>도큐먼트 타입을 선언한다.</li>
	<li>네임 스페이스를 선언한다.</li>
	<li>컨텐츠 타입을 선언한다.</li>
	<li>모든 태그는 계층에 맞게 싸고 있다.</li>
</ul>
```

![Untitled](html%2022%2006%2024-%2064b543fc25ac4aa382ce769045ab403b/Untitled%206.png)

- 블럭요소

- 리스트 스타일

```css
ul{list-style: disc;}
/* disc가 기본값 */
ul{list-style: circle;}
ul{list-style: square;}
ul{list-style: none;}
/* 없애놓고 쓰는 경우가 더 많음 */
```

- 리스트 포지션

```css
ul{list-style-position: inside;}
/* 블릿의 위치 안 쪽으로 */
```

- 리스트 스타일 이미지

```css
ul{list-style-image: url(./images/a1.jpg);}
/* 블릿을 이미지로 */
```

- **li 안에는 다 넣을 수 있다!!!!(div 급으로)**
- 글로벌 네비게이션 만들기(ul>li>ul>li…)

```html
ul>li*3
```

### 적용 - global nav

```html
<div>
     <h3>grobal nav</h3>
         <ul>
             <li><a href="#">1depth 01</a>
                 <ul>
                     <li>2depth 01</li>
                     <li>2depth 02</li>
                     <li>2depth 03</li>
                 </ul>
             </li>
             <li>1depth 02</li>
             <li>1depth 03</li>
             <li>1depth 04</li>
         </ul>
</div>
```

사진 자동 전환 메뉴 >> ul

어떤 UI컨텐츠가 2개 이상 반복될 때 ul

- 조직도

## ol

1. order list, 순서 있는 리스트(1. 2. 3. …)
2. ol 직계 자식은 li만 가능

```css
ol{list-style: decimal;}
/* 기본 */
ol{list-style: upper-roman;}
/* 로마 대문자 */
ol{list-style: lower-alpha;}
/* 영어 소문자 */
```

1. ol도 ul처럼 li내부에 중첩가능 
2. 순서가 꼭! 필요할 때
3. 프로세스, 절차, 순위차트 등

## dl - <dl><dt><dd>

- 정의형 목록(description list)
- 블럭요소
- 직계자식은 dt, dd만 올 수 있다
- dt,dd **최소 1개씩**은 있어야 한다
- 순서 지켜야함
- 접근성이 좋아진다
- 헤딩으로(목차로) 넣기엔 너무 자잘한 제목

- dt(decription title)
- dd는 직전dt의 리스트로 귀속된다
- dd는 여러개 사용할 수 있다
- dd 내부에 **중첩 불가**
- dl이나 dd 내부에 ul, ol 넣을 수 없다
- dt,dd 내부에는 인라인 요소만 올 수 있다

예시)

![Untitled](html%2022%2006%2024-%2064b543fc25ac4aa382ce769045ab403b/Untitled%207.png)