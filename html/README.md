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

##  warpper / contain box 
감싸는 wrapper, container 박스 만들면 유용함   
모든 <div>는 display: block 가짐 (가로행 전부 차지)

##  float: left 
요소를 붕 띄워서 왼쪽 정렬  

##  clear: both 
float 다음에 오는 요소에게 주면 float으로 발생하는 이상한 현상 해결가능

##  float: none 
버그예방차원에서 좋음

##  크기 % 
내 부모 태그(나를 감싸고 있는)의 ~에 % 만큼 차지
<br>
<br>

# 레이아웃 만들기 : inline-block

## inline-block
display: block (한 행을 전부 차지)  
display: inline-block (내 크기만큼 차지)  
inline-block 사용하려면 박스사이에 공백도 없어야 됨

## inline-block 공백제거 방법
박스사이에 주석기호 넣기 <!---->  
부모태그에 font-size: 0px 넣기  
자식태그에 font-size 지정해주면 글씨 보임  
(참고) 부모 태그로 inherit 되는 스타일은 중요도 가장 낮음

## inline-block 박스 안에 글
inline-block 박스에 <p></p> 를 사용하여 글을 쓰면 이상해짐  
baseline(글씨쓸 때 기준선)이 옆에 존재하면 inline-block 요소들이 baseline 위에 오려고 함

## 요약
inline-block 은 자기 크기만큼 자리차지  
공백제거 필요
주변에 글이 있으면 위치 오류남

## 진도가 안나간다
열심히 하자
layout css 적용 문제 해결하기