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