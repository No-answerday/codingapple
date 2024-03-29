# 230410

## Javascript 
html 조작과 변경   
document.getElementById('hello').innerHTML = '안녕';  
html문서 의(.) id가 hello인 요소 찾아와 그거의 내부 html을 '안녕'으로  
등호 : 오른쪽을 왼쪽에 넣으라는 뜻  
<Br>
.getElementById('hello') : 셀렉터  
.innerHTML / .style / .color : 메소드(함수)  
<br>
프로그래밍은 정확하고 구체적으로 해야 됨

## UI 만드는 step
1. HTML/CSS로 미리 디자인  
2. 필요할 떄 보여달라는 코드(JS)


## function
긴 코드 축약하고 싶을 때 사용 / 재사용 가능  
작명은 구체적으로, 주로 영어 camelCase로  
function 작명 () {}  
<Br>
TIP
1. 조작 할 html의 하단에 코드를 짜야 잘 실행됨  
2. 셀렉터 오타 주의 (크롬-검사-console : ~~~ of null error 확인)  
3. 기본 문법 오타 주의

##
문자는 '' 안에

## 파라미터(parameter) 
함수가 호출 될 때 함수로 전달되는 값  
function 작명(parameter) {} 


# 230411

## 
getElementsByClassName('클래스명')[순서] :  
일치하는 class가 들어있는 모든 html 요소를 찾는 셀렉터  
몇 번째 요소를 바꿀지 [순서]를 꼭 뒤에 붙여야함  
[0]  : 위에서부터 첫번째 요소, [1] : 위에서부터 두번째 요소 ...

## addEventListener
document.getElementById('close').addEventListener('click',function(){});  
문서 내 ''에 해당하는 Id를 찾아 'click'하면 함수를 실행해라

## event 
유저가 웹페이지에서 클릭, 스크롤, 키보드 입력, 드래그 등을 하는 것  
<br>
click : 클릭  
mouseover : 마우스 갖다대기  
scroll : 스크롤  
키입력 : keydown  
<br>
https://developer.mozilla.org/en-US/docs/Web/Events

## 콜백함수
파라미터자리에 들어가는 함수

## Bootstrap

## 클래스명 추가 / 제거
.classList.add('클래스명')  
.classList.remove('클래스명')

## toggle
있으면 제거, 없으면 추가해라

## querySelector
CSS 선택자를 사용하여 문서 내에 원하는 요소를 찾아 반환하는 셀렉터  
<br>
document.querySelector()  
('#IdName') : id 속성이 IdName 인 요소를 선택  
('.className') : class 속성이 className 인 요소를 선택  
<br>
querySelector()는 문서 내의 해당하는 첫번째 속성을 가져옴  
querySelectorAll()는 문서 내의 해당하는 모든 속성을 가져옴, [숫자]를 통해 원하는 위치를 찾을 수 있음

## jQuery
javascript 축약 라이브러리  
querySelector('.') : $('.') => 모든 요소 찾음  
.innerHTML : .html  
.css('color', 'red')  
.addClass()  
.removeClass()  
.toggleClass()  
.addEventListenr() : .on  
<br>
jQuery를 사용하면 뒤에 jQuery함수만 사용가능  
querySelector를 사용하면 뒤에 자바스크립트함수만 사용가능

## 외부 스크립트 위치
</body> 바로 위에 넣는게 좋음

## UI에 애니메이션 추가
JS에 넣어도 가능하지만 성능향상을 위해 CSS로만 처리하는게 좋음

## one-way UI 애니메이션
A상태 -> B상태  
1. 시작스타일  
2. 최종스타일  
(class로)  
3. 원할 때 최종스타일로 변하라고 JS 코드  
4. 시작스타일에 transiotion 추가  


# 230412

## 조건문
if(조건){조건이 참일 때 실행 할 코드}  
else{위 조건이 참이 아닐 때 실행 할 코드}

## 비교연산자
<, <=, =>, >
== : 같다

## input 공백
document.getElementById().value; : 유저가 <input>에 입력한 값

## alert
알림창

## 폼전송 막기
e.preventDefault();


# 230413

## else if
조건식을 연달아 쓰고 싶으면 사용 (사용 횟수 상관 X)  
앞의 조건식이 참이면 else문 실행 X


# 230414

## addEventListener
addEventListener('input')  : <input>에 입력한 값이 바뀔 때 발생  
addEventListener('change') : <input>에 입력한 값이 바뀌고 포커스를 잃을 때 발생

## if & boolean
if문 안에는 true / false (boolean) 넣어야 잘 됨

## 비교연산자
!= : 다름  
== : 같음, 느슨한 비교  
=== : 같음, 엄격한 비교 (type까지 같아야 됨)  
!== : 다름, 엄격한 비교 (type까지 같아야 됨)  

&& : 그리고 (and)
|| : 이거나 (or)

## true / false 로 인식자는 자료
truthy 자료  : 0 제외한 숫자, '문자', [], {}  
falsy 자료 : 0, '', null, undefined, NaN


# 230415

## 변수
변수 선언 : 변수를 만드는 것  
변수 할당 : 변수에 자료 넣기  
변수 범위 : 함수 안에서 변수를 만들 경우 함수 내부에서만 사용 가능   
변수 재할당 가능

## var
변수문법  
var 변수명 = 넣을 자료;  
모든 자료 넣을 수 있음  
재선언 O  
재할당 O  
범위 function  

## let
재선언 X  
재할당 O  
범위 {}

## const
재선언 X  
재할당 X  
범위 {}  
변하면 안되는 값을 보관하기 좋음


## 변수에 +1 하는 법
변수++  
변수+=1  
변수=변수+1

## 연산자 %
나눈 후 나머지  
ex : 4%3 = 1

## Bootstrap UI style
스타일 바꾸려면 class명을 수정하는게 좋음


# 230421

## setTimeout
x초 후에 코드 실행하기  
setTimeout(function(){실행코드}, ms)  

## setInterval
x초마다 코드 실행하기  
setTimeout(function(){실행코드}, ms)

## JS 문법 vs 브라우저 사용법

Javascript 문법 -> var let const if function  
웹브라우저 사용법 ->   
document.querySelector()  
alert()  
setTimeout()  
addEventListener()

## 콜백함수 참고
콜백함수 : 함수 파라미터에 들어가는 함수  
다른 곳에 만든 함수를 집어넣어도 작동됨

## clearTimour
타이머 삭제

# 230423

## 문자 검사
'문자'.includes('찾을단어')  
찾는 문자를 검색해서 있으면 true, 없으면 false  
단순한 검사만 가능  
한글, 영어, a로 끝나는지 ... 는 알 수가 없음

## 정규표현식(regular expression)
정규식은 문자를 검사하고 싶을 떄 사용함  
/정규식/.test(정규식으로 검사할 문자)
/abc/ : abc라는 문자가 있냐  
/abc/.test('abcde') : true

## 정규식 문법
1. []  
/[]/.test('') : []로 문자 범위 지정가능  
/[a-d]/.test('aefg') : true  
/[가-다]/.test('다라마바') : true  
/[a-zA-Z]/.test('') : 아무 알파벳 하나
/[ㄱ-ㅎ가-힣ㅏ-ㅣ]/.test('') : 아무 한글 하나  

2. \S  
백슬래시S : 특수문자 포함 아무 문자 하나  
/\S/.test('abcde') : true  

3. ^ , $  
^a : a로 시작하는지 검사  
e$ : e로 끝나는지 검사  

4. |  
| : or, 또는  
/(e|f)/.test('abcde') : true, e 또는 f 있는지 검사  

5. /+/  
/a+/ : 뒤에 오늘 글자들도 a와 일치하면 반복해서 쭉 찾아달라는 뜻  
aaaaa 같은 문자를 찾을 때 사용  

6. . 사용 시 주의점  
/\S+@\S+\.\S+/ : 이메일을 찾기 위한 간단한 정규식  
.com, .net을 찾기 위해서 .을 사용해야 하는데 .은 특수문법  
따라서 백슬래쉬를 앞에 붙여야 찾을 수 있음 .\


# 230426

## function
1. 긴 코드 축약해서 사용가능  
2. 파라미터 추가가능  
3. return

## return
함수를 쓰고 그자리에 무엇인가를 반환함  
무엇인가는 아무거나 상관없음  
함수종료 기능 : 함수 내 return 아래 코드는 실행 X  


## 소수점 있는 숫자 연산 시 주의점
컴퓨터는 이진법을 사용  
소수점을 이진법으로 연산 할 경우 무한히 반복됨 -> 1.0001100110011....  
그래서 근사치로 저장하는데 이 떄문에 정확한 숫자가 아님 -> 1.1 + 0.3 = 1.4000000000001  

## 정확한 소수점 숫자 연산
1. 소수점을 전부 10 곱해서 연산 후 10으로 나눔   
2. 라이브러리 사용  
3. 연산결과를 반올림 (오차가 매우 작기 떄문)  

## 반올림
숫자.toFixed(자리 수)  
toFixed 사용 시 문자취급  
parseFloat(), parseInt() 사용해서 숫자로 변경해야함

## 자바스크립트 + 연산자 특징
'문자' + 123 => '문자123'  
'문자' + '문자' => '문자문자'

# 230429

## scroll 이벤트리스너
window.addEventListener('scroll', function(){}) : 스크롤이 될 때마다 함수 실행  
window.scrollY : 유저가 얼마나 스크롤바 내렸나  
window.scrollTo(x,y) : 강제로 스크롤하기  
window.scrollBy(x,y) : 현재 위치부터 강제로 스크롤하기    
<!-- $(window).scrollTop() : jQuery, 현재 스크롤바 위치출력 -->

## overflow-y : scroll
style로서 내용이 길어지면 스크롤바 생성


