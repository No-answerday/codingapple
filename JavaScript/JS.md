# 230410

##
Javascript : html 조작과 변경 
document.getElementById('hello').innerHTML = '안녕';
html문서 의(.) id가 hello인 요소 찾아와 그거의 내부 html을 '안녕'으로
등호 : 오른쪽을 왼쪽에 넣으라는 뜻

.getElementById('hello') : 셀렉터
.innerHTML / .style / .color : 메소드(함수)

프로그래밍은 정확하고 구체적으로 해야 됨

## 
UI 만드는 step
1. HTML/CSS로 미리 디자인
2. 필요할 떄 보여달라는 코드(JS)


##
function : 
긴 코드 축약하고 싶을 때 사용 / 재사용 가능
작명은 구체적으로, 주로 영어 camelCase로
function 작명 () {}

TIP
1. 조작 할 html의 하단에 코드를 짜야 잘 실행됨
2. 셀렉터 오타 주의 (크롬-검사-console : ~~~ of null error 확인)
3. 기본 문법 오타 주의

##
문자는 '' 안에

파라미터(parameter) : 함수가 호출 될 때 함수로 전달되는 값
function 작명(parameter) {} 
