---
title: html과 css속성
date: "2022-07-14T22:12:03.284Z"
description: ""
---


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

## 스페이스바 역할(비추)

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







