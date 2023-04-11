# 230410

## Javascript 
html 조작과 변경 
document.getElementById('hello').innerHTML = '안녕';
html문서 의(.) id가 hello인 요소 찾아와 그거의 내부 html을 '안녕'으로
등호 : 오른쪽을 왼쪽에 넣으라는 뜻

.getElementById('hello') : 셀렉터
.innerHTML / .style / .color : 메소드(함수)

프로그래밍은 정확하고 구체적으로 해야 됨

## UI 만드는 step
1. HTML/CSS로 미리 디자인
2. 필요할 떄 보여달라는 코드(JS)


## function
긴 코드 축약하고 싶을 때 사용 / 재사용 가능
작명은 구체적으로, 주로 영어 camelCase로
function 작명 () {}

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

click : 클릭
mouseover : 마우스 갖다대기
scroll : 스크롤
키입력 : keydown

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

document.querySelector()
('#IdName') : id 속성이 IdName 인 요소를 선택
('.className') : class 속성이 className 인 요소를 선택

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