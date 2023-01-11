##### 220809 HTML

HTML : 마크업 언어, 자료의 구조를 표현하기 위한 언어 / HyperText Markup Language


### <Tag>

<p>paragraph</p>

<h1>heading, 글제목</h1>

<img src="이미지경로"> // src : 속성

<button>버튼</button>

<a href="링크주소">링크</a>

<ul>리스트, unorderd list</ul>

<ul>
  <li>항목, list item</li>
</ul>

<ul>리스트, orderd list</ul>

### 
1. 웹페이지 만들 때 모든 요소는 태그 안에 넣음
2. 일부 태그는 속성(src) 기입 가능
3. 태그 안에 태그도 가능


### HTML 꾸미는 법
style 속성으로 꾸밈
style="값;"

### 이미지 가운데 정렬
display: block;
margin-left: auto;
margin-right: auto;

### 글자 스타일링
글자 크기 font-size
폰트 종류 font-family
글자 색   color
자간      letter-spacing
글자 정렬 text-align
글자 굵기 font-weight 또는 <strong></strong>

<span> : 글자를 감쌀수 있는 별 뜻 없는 태그
(참고) span 태그는 display : inline 이라는 스타일 속성을 내포하고 있으며,
      display : inline을 가지고 있는 요소는 폭, 높이 등을 단독으로 결정할 수 없습니다
      폭, 높이를 주고싶으면 얘를 감싸고 있는 <p>에 주십시오

##### 220809 CSS

### CSS파일에 스타일 보관하기
1. <link>로 CSS 파일 연결
2. CSS 파일에 style 작성
3. HTML 파일에서 작명한거 사용, class=""

(참고) class는 . 찍고 작명, 이름 중복 X
태그 이름을 사용하면 태그에 해당하는 전체 스타일 적용
#special { } , id로 css 축약하여 스타일 적용 // 사용 잘 안함

### CSS selector
.class : class selector // 10점
tag : tag selector      // 1점
#id : id selector       // 100점

선택자가 겹칠 경우 우선순위가 높은 것으로 적용
(HTML에 직접 style="" 적용, 1000점) >>>> id >>> class >> tag

### div tag
상자 만드는 태그
margin (상하좌우 여백)
padding (상하좌우 안쪽 여백)
border (테두리)
border-radius (테두리 둥글게)

<div>, <p>, <h> 의 특징 >>> display: block; 기본으로 있음, 가로행을 전부 차지

### inherit 상속
일부 스타일은 부모에게 적용 시 자동으로 자식 요소에게 상속되어 적용됨
font-size, font-family, color ... 


# 레이아웃 만들기 : 호환성 좋은 float

감싸는 wrapper, container 박스 만들면 유용함
모든 <div>는 display: block 가짐 (가로행 전부 차지)

float: left -> 요소를 붕 띄워서 왼쪽 정렬

clear: both -> float 다음에 오는 요소에게 주면 float으로 발생하는 이상한 현상 해결가능
float: none -> 버그예방차원에서 좋음

크기 % : 내 부모 태그(나를 감싸고 있는)의 ~에 % 만큼 차지