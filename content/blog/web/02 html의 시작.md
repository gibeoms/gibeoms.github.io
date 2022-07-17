---
title: html의 시작
date: "2022-07-13T22:12:03.284Z"
description: ""
---


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

