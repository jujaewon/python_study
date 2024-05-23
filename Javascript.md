Javascript
---

ECMAScript : Ecma International이 정의하고 있는 표준화된 스크립트 프로그래밍 언어 명세
- 스크립트 언어가 준수해야 하는 규칙, 세부사항 등을 제공

JavaScript는 ECMAScript 표준을 구현한 구체적인 프로그래밍 언어

ECMAScript5의 명세를 기반으로 하여 웹 브라우저나 Node.js와 같은 환경에서 실행됨

ECMAScript는 JavaScript의 표준이며, JavaScript는 ECMAScript 표준을 따르는 구체적인 프로그래밍 언어

ECMAScript는 언어의 핵심을 정의하고, JavaScript는 ECMAScript 표준을 따라 구현된 언어로 사용됨

ECMAScript5에서 안정성과 생산성을 크게 높임

ECMAScript6에서 객체지향 프로그래밍 언어로써 많은 발전을 이루어, 역사상 가장 중요한 버전으로 평가됨

웹 브라우저에서의 JavaScript : 웹 페이지의 동적인 기능을 구현

DOM : 웹 페이지(Document)를 구조화된 객체로 제공하여 프로그래민 언어가 페이지 구조에 접근할 수 있는 방법을 제공
- 문서 구조, 스타일, 내용 등을 변경할 수 있도록 함
  
DOM에서 모든 요소, 속성, 텍스트는 하나의 객체

모두 document 객체의 자식으로 구성됨

브라우저 HTML 문서를 해석하여 DOM tree라는 객체 트리로 구조화
- 객체 간 상속 구조가 존재

DOM 핵심 : 문서의 요소들을 객체로 제공하여 다른 프로그래밍 언어에서 접근하고 조작할 수 있는 방법을 제공하는 API

'document' 객체
- 웹 페이지 객체
- DOM Tree의 진입점
- 페이지를 구성하는 모든 객체 요소를 포함

DOM 조작 순서
1. 조작하고자 하는 요소를 선택(또는 탐색)
2. 선택된 요소의 콘텐츠 또는 속성을 조작

선택 메서드
- document.querySelector() : 요소 한 개 선택
- document.querySelectorAll() : 요소 여러 개 선택

document.querySelector(selector) : 제공한 선택자와 일치하는 element 한 개 선택
- 제공한 CSS selector를 만족하는 첫 번째 element 객체를 반환(없다면 null 반환)

document.querySelectorAll(selector) : 제공한 선택자와 일치하는 여러 element를 선택
- 제공한 CSS selector를 만족하는 NodeList를 반환

속성(attribute) 조작
1. 클래스 속성 조작
2. 일반 속성 조작

클래스 속성 조작
'classList' property : 요소의 클래스 목록을 DOMTokenList(유사 배열) 형태로 변환

classList 메서드
- element.classList.add() : 지정한 클래스 값을 추가
- element.classList.remove() : 지정한 클래스 값을 제거
- element.classList.toggle() : 클래스가 존재한다면 제거하고 false를 반환(존재하지 않으면 클래스를 추가하고 true 반환)

속성 조작 메서드
- Element.getAttribute() : 해당 요소에 지정된 값을 반환(조회)
- Element.setAttribute(name, value) : 지정된 요소의 속성 값을 설정, 속성이 이미 있으면 기존 값을 갱신(그렇지 않으면 지정된 이름과 값으로 새 속성이 추가)
- Element.removeAttribute() : 요소에서 지정된 이름을 가진 속성 제거

'textContent' property : 요소의 텍스트 콘텐츠를 표현

DOM 요소 조작 메서드
- document.createElement(tagName) : 작성한 tagName의 HTML 요소를 생성하여 반환
- Node.appendChild() : 한 Node를 특정 부모 Node의 자식 NodeList 중 마지막 자식으로 삽입, 추가된 Node 객체를 반환
- Node.removeChild() : DOM에서 자식 Node를 제거, 제거된 Node를 반환

'style' property : 해당 요소의 모든 style 속성 목록을 포함하는 속성

Node 
1. DOM의 기본 구성 단위
2. DOM 트리의 각 부분은 Node라는 객체로 표현됨
- Document Node : HTML 문서 전체를 나타내는 노드
- Element Node : HTML 요소를 나타내는 노드
- Text Node : HTML 텍스트, Element Node 내의 텍스트 컨텐츠를 나타냄
- Attribute : HTML 요소의 속성을 나타내는 노드

NodeList 
- DOM 메서드를 사용해 선택한 Node의 목록
- 배열과 유사한 구조를 가짐
- Index로만 각 항목에 접근 가능
- 다양한 배열 메서드 사용 가능
- querySelectorAll()에 의해 반환되는 NodeList는 DOM의 변경사항을 실시간으로 반영하지 않음

Element
- Node의 하위 유형
- Element는 DOM 트리에서 HTML 요소를 나타내는 특별한 유형의 Node
- 예를 들어, <p>, <div>, <span>, <body>등의 HTML 태그들이 Element 노드를 생성
- Node의 속성과 메서드를 모두 가지고 있으며 추가적으로 요소 특화된 기능(예 : className, innerHTML, id등)을 가지고 있음
- 모든 Element는 Node이지만, 모든 Node가 Element인 것은 아님

Parsing(구문 분석, 해석) : 브라우저가 문자열을 해석하여 DOM Tree로 만드는 과정

식별자(변수명) 작성 규칙
- 반드시 문자, 달러($) 또는 밑줄(_)로 시작
- 대소문자를 구분
- 예약어 사용 불가(for, if, function 등)

카멜 케이스(camelCase) : 변수, 객체, 함수에 사용

파스칼 케이스(PascalCase) : 클래스, 생성자에 사용

대문자 스네이크 케이스(SNAKE_CASE) : 상수(constants)에 사용

변수 선언 키워드 : let, const, var

let 
- 블록 스코프(block scope)를 갖는 지역 변수를 선언
- 재할당 가능
- 재선언 불가능
- ES6에서 추가

const
- 블록 스코프를 갖는 지역 변수를 선언
- 재할당 불가능
- 재선언 불가능
- ES6에서 추가

블록 스코프(block scope)
- if, for, 함수 등의 '중괄호({}) 내부'를 가리킴
- 블록 스코프를 가지는 변수는 블록 바깥에서 접근 불가능

변수 선언 키워드 정리
- 기본적으로 const 사용을 권장
- 재할당이 필요한 변수는 let으로 변경해서 사용

데이터 타입
- 원시 자료형(Primitive type) : Number, String, Boolean, undefined, null
- 참조 자료형(Reference type) : Objects(Object, Array, Function)

원시 자료형 : 변수에 값이 직접 저장되는 자료형(불변, 값이 복사)
- 변수에 할당될 때 값이 복사됨 : 변수 간에 서로 영향을 미치지 않음

참조 자료형 : 객체의 주소가 저장되는 자료형(가변, 주소가 복사)
- 객체를 생성하면 객체의 메모리 주소를 변수에 할당 : 변수 간에 서로 영향을 미침

Number : 정수 또는 실수형 숫자를 표현하는 자료형

String : 텍스트 데이터를 표현하는 자료형
- '+' 연산자를 사용해 문자열끼지 결함
- 곱셈, 나눗셈, 뺄셈 불가능

Template literals(템플릿 리터럴)
- 내장된 표현식을 허용하는 문자열 작성 방식
- Backtick(``)을 이용하며, 여러 줄에 걸쳐 문자열을 정의할 수도 있고 JavaScript의 변수를 문자열 안에 바로 연결할 수 있음
- 표현식은 '$'와 중괄호(${expression})로 표기
- ES6+ 부터 지원

null : 변수의 값이 없음을 의도적으로 표현할 때 사용

undefined : 변수 선언 이후 직접 값을 할당하지 않으면 자동으로 할당됨

Boolean(true/false)
- 조건문 또는 반복문에서 Boolean이 아닌 데이터 타입은 "자동 형변환 규칙"에 따라 true 또는 false로 변환됨

undefined, null : 항상 false

Number
- false : 0, -0, NaN
- true : 나머지 모든 경우

String
- false : 빈 문자열
- true : 나머지 모든 경우

할당 연산자
- 오른쪽에 있는 피연산자의 평가 결과를 왼쪽 피연산자에 할당하는 연산자
- 단축 연산자 지원

증가 연산자(++)
- 피연산자를 증가(1을 더함)시키고 연산자의 위치에 따라 증가하기 전이나 후의 값을 반환

감소 연산자(--)
- 피연산자를 감소(1을 뺌)시키고 연산자의 위치에 따라 감소하기 전이나 후의 값을 반환

+= 또는 -=와 같이 더 명시적인 표현으로 작성 하는 것을 권장

비교 연산자
- 피연산자들(숫자, 문자, Boolean 등)을 비교하고 결과 값을 boolean으로 반환하는 연산자

동등 연산자(==)
- 두 피연산자가 같은 값으로 평가되는지 비교 후 boolean 값을 반환
- '암묵적 타입 변환' 통해 타입을 일치시킨 후 같은 값인지 비교
- 두 피연산자가 모두 객체일 경우 메모리의 같은 객체를 바라보는지 판별

일치 연산자(===)
- 두 피연산자의 값과 타입이 모두 같은 경우 true를 반환
- 같은 객체를 가리키거나, 같은 타입이면서 같은 값인지를 비교
- 엄격한 비교가 이뤄지며 암묵적 타입 변환이 발생하지 않음
- 특수한 경우를 제외하고는 동등 연산자가 아닌 일치 연산자 사용 권장

논리 연산자
- and 연산 : &&
- or 연산 : ||
- not 연산 : !
- 단축 평가 지원

if : 조건 표현식의 결과값을 boolean 타입으로 변환 후 참/거짓을 판단

조건(삼항) 연산자
- 세 개의 피연산자를 받는 유일한 연산자
- 앞에서부터 조건문, 물음표(?), 조건문이 참일 경우 실행할 표현식, 콜론(:), 조건문이 거짓일 경우 실행할 표현식이 배치

반복문(while, for, for in, for of)
- while : 조건문이 참이면 문장을 계속해서 수행
- for : 특정한 조건이 거짓으로 판별될 때까지 반복
- for in : 객체의 열거 가능한 속성(property)에 대해 반복
- for of : 반복 가능한 객체(배열, 문자열 등)에 대해 반복

배열 반복과 for in 
- 배열의 인덱스는 정수 이름을 가진 열거 가능한 속성
- for in은 정수가 아닌 이름과 속성을 포함하여 열거 가능한 모든 속성을 반환
- 내부적으로 for in은 배열의 반복자 대신 속성 열거를 사용하기 때문에 특정 순서에 따라 인덱스를 반환하는 것을 보장할 수 없음
- 인덱스의 순서가 중요한 배열에서는 사용하지 않음
- 배열에서는 for 반복, for of 반복을 사용
  
for 문
- for (let i = 0; i < arr.length; i ++) { }의 경우에는 최초 정의한 i를 "재할당"하면서 사용하기 때문에 const를 사용하면 에러 발생
  
for in, for of
- 재할당이 아니라, 매 반복마다 다른 속성 이름이 변수에 지정되는 것이므로 const를 사용해도 에러가 발생하지 않음
- 단, const 특징에 따라 블록 내부에서 변수를 수정할 수 없음

while 
- 연관 키워드 : break, continue
- 스코프 : 블록 스코프

for
- 연관 키워드 : break, continue
- 스코프 : 블록 스코프

for in
- 연관 키워드 : object 순회
- 스코프 : 블록 스코프

for of
- 연관 키워드 : Iterable 순회
- 스코프 : 블록 스코프

세미콜론(semicolon)
- 자바스크립트는 세미콜론을 선택적으로 사용 가능
- 세미콜론이 없으면 ASI에 의해 자동으로 세미콜론이 삽입됨(ASI(Automatic Semicolon Insertion, 자동 세미콜론 삽입 규칙))

변수 선언 키워드 - 'var'
- 재할당 가능 & 재선언 가능
- "호이스팅"되는 특성으로 인해 예기치 못한 문제 발생 기능
- 함수 스코프(function scope)를 가짐
- 변수 선언 시 var, const, let 키워드 중 하나를 사용하지 않으면 자동으로 var로 선언됨

함수 스코프(function scope)
- 함수의 중괄호 내부를 가리킴
- 함수 스코프를 가지는 변수는 함수 바깥에서 접근 불가능

호이스팅(hoisting)
- 변수를 선언 이전에 참조할 수 있는 현상
- 변수 선언 이전의 위치에서 접근 시 undefined를 반환
- JavaScript에서 변수들은 실제 실행시에 코드의 최상단으로 끌어 올려지게 되며(hoisted) 이러한 이유 때문에 var로 선언된 변수는 선언 시에 undefined로 값이 초기화되는 과정이 동시에 발생

NaN을 반환하는 경우 예시
1. 숫자로서 읽을 수 없음(Number(undefined))
2. 결과가 허수인 수학 계산식(Math.sqrt(-1))
3. 피연산자가 NaN(7**NaN)
4. 정의할 수 없는 계산식(0*Infinity)
5. 문자열을 포함하면서 덧셈이 아닌 계산식('가'/3)

함수(Function) : 참조 자료형에 속하며 모든 함수는 Function object

함수 구조
- 함수의 이름
- 함수의 매개변수
- 함수의 body를 구성하는 statement
- return 값이 없다면 undefined를 반환

함수 정의 2가지 방법 : 선언식(function declaration), 표현식(function expression)

함수 표현식 특징
- 함수 이름이 없는 '익명 함수'를 사용할 수 있음
- 선언식과 달리 표현식으로 정의한 함수는 호이스팅 되지 않으므로 함수를 정의하기 전에 먼저 사용할 수 없음

함수 선언식 : 익명 함수 사용 불가능, 호이스팅 있음

매개변수 정의 방법 : 기본 함수 매개변수, 나머지 매개변수

기본 함수 매개변수 : 값이 없거나 undefined가 전달된 경우 이름 붙은 매개변수를 기본값으로 초기화

나머지 매개변수 : 임의의 수의 인자를 '배열'로 허용하여 가변 인자를 나타내는 방법

작성 규칙
- 함수 정의 시 나머지 매개변수 하나만 작성할 수 있음
- 나머지 매개변수는 함수 정의에서 매개변수 마지막에 위치해야 함

매개변수 개수 > 인자 개수 : 누락된 인자는 undefined로 할당

매개변수 개수 > 인자 개수 : 초과 입력한 인자는 사용하지 않음

전개 구문(...)
- 배열이나 문자열과 같이 반복 가능한 항목을 펼치는 것(확장, 전재)
- 전개 대상에 따라 역할이 다름
  - 배열이나 객체의 요소를 개별적인 값으로 분리하거나 다른 배열이나 객체의 요소를 현재 배열이나 객체에 추가하는 등
1. 함수와의 사용
- 함수 호출 시 인자 확장
- 나머지 매개변수(압축)
2. 객체와의 사용(객체 파트에서 진행)
3. 배열과의 활용(배열 파트에서 진행)

화살표 함수 표현식(Arrow function expressions) : 함수 표현식의 간결한 표현법

1. function 키워드 제거 후 매개변수와 중괄호 사이에 화살표(=>) 작성
2. 함수의 매개변수가 하나 뿐이라면, 매개변수의 `()` 제거 가능(단, 생략하지 않는 것을 권장)
3. 함수 본문의 표현식이 한 줄이라면, `{}`와 `return` 제거 가능

Object : 키로 구분된 데이터 집합(data collection)을 저장하는 자료형

객체 구조
- 중괄호를 이용해 작성
- 중괄호 안에는 key: value 쌍으로 구성된 속성(property)를 여러 개 작성 가능
- key는 문자형만 허용
- value는 모든 자료형 허용

속성 참조
- 점('.', chaining operator)또는 대괄호([])로 객체 요소 접근
- key 이름에 띄어쓰기 같은 구분자가 있으면 대괄호 접근만 가능

'in' 연산자 : 속성이 객체에 존재하는지 여부를 확인

Method : 객체 속성에 정의된 함수
- object.method() 방식으로 호출
- 메서드는 객체를 '행동'할 수 있게 함
- 'this' 키워드를 사용해 객체에 대한 특정한 작업을 수행 할 수 있음

'this' keyword 
- 함수나 메서드를 호출한 객체를 가리키는 키워드
  - 함수 내에서 객체의 속성 및 메서드에 접근하기 위해 사용

호출 방법 : 단순 호출 -> 대상 : 전역 객체
호출 방법 : 메서드 호출 -> 대상 : 메서드를 호출한 객체

화살표 함수는 자신만의 this를 가지지 않기 때문에 외부 함수에서의 this 값을 가져옴

1. JavaScript에서 this는 함수가 "호출되는 방식"에 따라 결정되는 현재 객체를 나타냄
2. JavaScript 함수는 호출될 때 this를 암묵적으로 전달 받음
3. Python의 self와 Java의 this가 선언 시 값이 이미 정해지는 것에 비해 JavaScript의 this는 함수가 호출되기 전까지 값이 할당되지 않고 호출 시에 결정됨(동적 할당)

단축 속성
- 키 이름과 값으로 쓰이는 변수의 이름이 같은 경우 단축 구문을 사용할 수 있음

단축 메서드
- 메서드 선언 시 function 키워드 생략 가능

계산된 속성(computed property name)
- 키가 대괄호([])로 둘러싸여 있는 속성
- 고정된 값이 아닌 변수 값을 사용할 수 있음

구조 분해 할당(destructing assignment)
- 배열 또는 객체를 분해하여 속성을 변수에 쉽게 할당할 수 있는 문법
- '함수의 매개변수'로 객체 구조 분해 할당 활용 가능

Object with '전개 구문'
- "객체 복사" : 객체 내부에서 객체 전개
- 얕은 복사에 활용 가능

유용한 객체 메서드 : Object.keys(), Object.values()

Optional chaining('?.')
- 속성이 없는 중첩 객체를 에러 없이 접근할 수 있음
- 만약 참조 대상이 null 또는 undefined라면 에러가 발생하는 것 대신 평가를 멈추고 undefined를 반환
- Optional chaining이 없다면 다음과 같이 '&&' 연산자를 사용해야 함

Optional chaining의 장점
- 참조가 누락될 가능성이 있는 경우 연결된 속성으로 접근할 때 더 짧고 간단한 표현식을 작성할 수 있음
- 어떤 속성이 필요한지에 대한 보증이 확실하지 않는 경우에 객체의 내용을 보다 편리하게 탐색할 수 있음

Optional chaining 주의사항
1. Optional chaining은 존재하지 않아도 괜찮은 대상에만 사용해야 함(남용 X)
- 왼쪽 평가대상이 없어도 괜찮은 경우에만 선택적으로 사용
2. Optional chaining 앞의 변수는 반드시 선언되어 있어야 함

Optional chaining 요약
1. obj?.prop : obj가 존재하면 obj.prop을 반환하고, 그렇지 않으면 undefined를 반환
2. obj?.[prop] : obj가 존재하면 obj[prop]을 반환하고, 그렇지 않으면 undefined를 반환
3. obj?.method() : obj가 존재하면 obj.method()를 호출하고, 그렇지 않으면 undefined를 반환

JSON(JavaScript Object Notation)
- Key-Value 형태로 이루어진 자료 표기법
- JavaScript의 Object와 유사한 구조를 가지고 있지만 JSON은 형식이 있는 "문자열"
- JavaScript에서 JSON을 사용하기 위해서는 Object 자료형으로 변경해야 함

new 연산자
- 사용자 정의 객체 타입을 생성
- 매개변수
1. constructor: 객체 인스턴스의 타입을 기술(명세)하는 함수
2. arguments: constructor와 함께 호출될 값 목록

Array : 순서가 있는 데이터 집합을 저장하는 자료 구조

배열 구조
- 대괄호([])를 이용해 작성
- 배열 요소 자료형 : 제약 없음
- length 속성을 사용해 배열에 담긴 요소가 몇 개인지 알 수 있음

주요 메서드
- push / pop : 배열 끝 요소를 추가 / 제거
- unshift / shift : 배열 앞 요소를 추가 / 제거

pop() : 배열 끝 요소를 제거하고, 제거한 요소를 반환
push() : 배열 끝에 요소를 추가
shift() : 배열 앞 요소를 제거하고, 제거한 요소를 반환
unshift() : 배열 앞에 요소를 추가

Array Helper Methods : 배열을 순회하며 특정 로직을 수행하는 메서드
- 메서드 호출 시 인자로 함수를 받는 것이 특징

forEach : 인자로 주어진 함수(콜백함수)를 배열 요소 각각에 대해 실행
map : 배열 내에 모든 요소 각각에 대해 함수(콜백함수)를 호출하고, 함수 호출 결과를 모아 새로운 배열을 반환

forEach 구조
arr.forEach(callback(item[, index[, array]]))

콜백함수는 3가지 매개변수로 구성
1. item: 처리할 배열의 요소
2. index: 처리할 배열 요소의 인덱스(선택 인자)
3. array: forEach를 호출할 배열(선택 인자)
반환 값: undefined

콜백 함수(Callback function) : 다른 함수에 인자로 전달되는 함수
- 외부 함수 내에서 호출되어 일종의 루틴이나 특정 작업을 진행

map 구조
arr.map(callback(item[, index[, array]]))

1. item: 처리할 배열의 요소
2. index: 처리할 배열 요소의 인덱스(선택 인자)
3. array: map를 호출할 배열(선택 인자)
반환 값: 배열의 각 요소에 대해 실행한 "callback의 결과를 모은 새로운 배열"
- 기본적으로 forEach 동작 원리와 같지만 forEach와 달리 새로운 배열을 반환함

forEach
- 간결하고 가독성이 높음
- callback 함수를 이용하여 각 요소를 조작하기 용이
- break, continue 사용 불가능

콜백함수 구조를 사용하는 이유
1. "함수의 재사용성 측면"
- 함수를 호출하는 코드에서 콜백 함수의 동작을 자유롭게 변경할 수 있음
- 예를 들어, map 함수는 콜백 함수를 인자로 받아 배열의 각 요소를 순회하며 콜백 함수를 실행
- 이때, 콜백 함수는 각 요소를 변환하는 로직을 담당하므로, map 함수를 호출하는 코드는 간결하고 가독성이 높아짐
2. 비동기적 처리 측면
- setTimeout 함수는 콜백 함수를 인자로 받아 일정 시간이 지난 후에 실행됨
- 이때, setTimeout 함수는 비동기적으로 콜백 함수를 실행하므로, 다른 코드의 실행을 방해하지 않음

배열은 키와 속성들을 담고 있는 참조 타입의 객체
배열은 인덱스를 키로 가지며 length 프로퍼티를 갖는 특수한 객체
배열의 요소를 대괄호 접근법을 사용해 접근하는 건 객체 문법과 같음
배열의 키는 숫자
숫자형 키를 사용함으로써 배열은 객체 기본 기능 이외에도 순서가 있는 컬렉션을 제어하게 해주는 특별한 메서드를 제공

event : 무언가 일어났다는 신호, 사건
- 모든 DOM 요소는 이러한 event를 만들어 냄

event object : DOM에서 이벤트가 발생했을 때 생성되는 객체

DOM 요소는 event를 받고 받은 event를 '처리'할 수 있음

event handler : 이벤트가 발생했을 때 실행되는 함수
- 사용자의 행동에 어떻게 반응할지를 JavaScript 코드로 표현한 것

.addEventListener() : 대표적인 이벤트 핸들러 중 하나
- 특정 이벤트를 DOM 요소가 수신할 때마다 콜백 함수를 호출

DOM 요소.addEventListener(수신할 이벤트, 콜백 함수)
- "대상에 특정 Event가 발생하면, 지정한 이벤트를 받아 할 일을 등록한다."

.addEventListener(type, handler)

type
- 수신할 이벤트 이름
- 문자열로 작성(ex. 'click')
  
handler
- 발생한 이벤트 객체를 수신하는 콜백 함수
- 콜백 함수는 발생한 Event object를 유일한 매개변수로 받음

요소에 addEventListener를 부착하게 되면 내부의 this 값은 대상 요소를 가리키게 됨(event 객체의 currentTarget 속성 값과 동일)

addEventListener의 콜백 함수 특징
- 발생한 이벤트를 나타내는 Event 객체를 유일한 매개변수로 받음
- 아무것도 반환하지 않음

버블링(Bubbling) 
- 한 요소에 이벤트가 발생하면, 이 요소에 할당된 핸들러가 동작하고, 이어서 부모 요소의 핸들러가 동작하는 현상
- 가장 최상단의 조상 요소(document)를 만날 때까지 이 과정이 반복되면서 요소 각각에 할당된 핸들러가 동작

이벤트가 정확히 어디서 발생했는지 접근할 수 있는 방법 : event.target, event.currentTarget

'target' & 'currentTarget' 속성

'target' 속성
- 이벤트가 발생한 가장 안쪽의 요소(target)를 참조하는 속성
- 실제 이벤트가 시작된 target 요소
- 버블링이 진행 되어도 변하지 않음

'currentTarget' 속성
- '현재' 요소
- 항상 이벤트 핸들러가 연결된 요소만을 참조하는 속성
- 'this'와 같음

.preventDefault() : 해당 이벤트에 대한 기본 동작을 실행하지 않도록 지정

화살표 함수는 자신만의 this를 가지지 않기 때문에 자신을 포함하고 있는 함수의 this를 상속 받음

Synchronous(동기) : 프로그램의 실행 흐름이 순차적으로 진행
- 하나의 작업이 완료된 후에 다음 작업이 실행되는 방식

Asynchronous(비동기) : 프로그램의 실행 흐름이 순차적이지 않으며, 작업이 완료되기를 기다리지 않고 다음 작업이 실행되는 방식
- 작업의 완료 여부를 신경 쓰지 않고 동시에 다른 작업들을 수행할 수 있음

Asynchronous 특징
- 병렬적 수행
- 당장 처리를 완료할 수 없고 시간이 필요한 작업들은 별도로 요청을 보낸 뒤 응답이 빨리 오는 작업부터 처리

Thread : 작업을 처리할 때 실제로 작업을 수행하는 주체로, multi-thread라면 업무를 수행할 수 있는 주체가 여러 개라는 의미

JavaScript는 한 번에 하나의 일만 수행할 수 있는 Single Thread 언어로 동시에 여러 작업을 처리할 수 없음

즉, JavaScript는 하나의 작업을 요청한 순서대로 처리할 수 밖에 없음

JavaScript Runtime : "JavaScript가 동작할 수 있는 환경(Runtime)"

JavaScript 자체는 Single Thread이므로 비동기 처리를 할 수 있도록 도와주는 환경이 필요

JavaScript에서 비동기와 관련한 작업은 "브라우저" 또는 "Node"와 같은 환경에서 처리

브라우저 환경에서의 JavaScript 비동기 처리 관련 요소
1. JavaScript Engine의 Call Stack
2. Web API
3. Task Queue
4. Event Loop

브라우저 환경에서의 JavaScript 비동기 처리 동작 방식
1. 모든 작업은 Call Stack(LIFO)으로 들어간 후 처리된다.
2. 오래 걸리는 작업이 Call Stack으로 들어오면 Web API로 보내 별도로 처리하도록 한다.
3. Web API에서 처리가 끝난 작업들은 곧바로 Call Stack으로 들어가지 못하고 Task Queue(FIFO)에 순서대로 들어간다.
4. Event Loop가 Call Stack이 비어 있는 것을 계속 체크하고 Call Stack이 빈다면 Task Queue에서 가장 오래된(가장 먼저 처리되어 들어온) 작업을 Call Stack으로 보낸다.

Call Stack
- 요청이 들어올 때마다 순차적으로 처리하는 Stack(LIFO)
- 기본적인 JavaScript의 Single Thread 작업 처리

Web API
- JavaScript 엔진이 아닌 브라우저에서 제공하는 runtime 환경
- 시간이 소요되는 작업을 처리(setTimeout, DOM Event, AJAX 요청 등)

Task Queue(Callback Queue)
- 비동기 처리된 Callback 함수가 대기하는 Queue(FIFO)

Event Loop
- 태스크(작업)가 들어오길 기다렸다가 태스크가 들어오면 이를 처리하고, 처리할 태스크가 없는 경우엔 잠드는, 끊임 없이 돌아가는 자바스크립트 내 루프
- Call Stack과 Task Queue를 지속적으로 모니터링
- Call Stack이 비어 있는지 확인 후 비어 있다면 Task Queue에서 대기 중인 오래된 작업을 Call Stack으로 Push

JavaScript는 한 번에 하나의 작업을 수행하는 Single Thread 언어로 동기적 처리를 진행

하지만 브라우저 환경에서는 Web API에서 처리된 작업이 지속적으로 Task Queue를 거쳐 Event Loop에 의해 Call Stack에 들어와 순차적으로 실행됨으로써 비동기 작업이 가능한 환경이 됨

AJAX(Asynchronous JavaScript + XML) : JavaScript의 비동기 구조와 XML 객체를 활용해 비동기적으로 서버와 통신하여 웹 페이지의 일부분만을 업데이트하는 웹 개발 기술

XMLHttpRequest 객체 : 서버와 상호작용할 때 사용하며 페이지의 새로고침 없이도 URL에서 데이터를 가져올 수 있음
- 사용자의 작업을 방해하지 않고 페이지의 일부를 업데이트
- 주로 AJAX 프로그래밍에 많이 사용됨

이벤트 핸들러는 비동기 프로그래밍의 한 형태
- 이벤트가 발생할 때마다 호출되는 함수(콜백 함수)를 제공하는 것
- XMLHttpRequest(XHR)는 JavaScript를 사용하여 서버에 HTTP 요청을 할 수 있는 객체
- HTTP 요청은 응답이 올 때까지의 시간이 걸릴 수 있는 작업이라 비동기 API이며, 이벤트 핸들러를 XHR 객체에 연결해 요청의 진행 상태 및 최종 완료에 대한 응답을 받음

Axios : JavaScript에서 사용되는 (Promise 기반) HTTP 클라이언트 라이브러리
- 서버와의 HTTP 요청과 응답을 간편하게 처리할 수 있도록 도와주는 도구

Axios 구조
- get, post 등 여러 http request method 사용 가능
- then 메서드를 사용해서 "성공하면 수행할 로직"을 작성
- catch 메서드를 사용해서 "실패하면 수행할 로직"을 작성

axios는 브라우저에서 비동기로 데이터 통신을 가능하게 하는 라이브러리
- 브라우저를 위해 XMLHttpRequest 생성
  
같은 방식으로 DRF로 만든 API 서버로 요청을 보내서 데이터를 받아온 후 처리할 수 있도록 함

비동기 처리의 단점
- 비동기 처리의 핵심은 Web API로 들어오는 순서가 아니라 작업이 완료되는 순서에 따라 처리한다는 것

비동기 콜백
- 비동기적으로 처리되는 작업이 완료되었을 때 실행되는 함수
- 연쇄적으로 발생하는 비동기 작업을 순차적으로 동작할 수 있게 함
- 작업의 순서와 동작을 제어하거나 결과를 처리하는 데 사용

비동기 콜백의 한계
비동기 콜백 함수는 보통 어떤 기능의 실행 결과를 받아서 다른 기능을 수행하기 위해 많이 사용됨

콜백 지옥(Callback Hell) : 비동기 처리를 위한 콜백을 작성할 때 마주하는 문제
(코드 작성 형태가 마치 "피라미드와 같다"고 해서 "Pyramid of doom(파멸의 피라미드)"라고도 부름)

콜백 함수는 비동기 작업을 순차적으로 실행할 수 있게 하는 반드시 필요한 로직

비동기 코드를 작성하다 보면 콜백 함수로 인한 콜백 지옥은 빈번히 나타나는 문제이며 이는 코드의 가독성을 해치고 유지 보수가 어려워 짐

Promise : JavaScript에서 비동기 작업의 결과를 나타내는 객체
- 비동기 작업이 완료되었을 때 결과 값을 반환하거나, 실패 시 에러를 처리할 수 있는 기능을 제공
- 콜백 지옥 문제를 해결하기 위해 등장한 비동기 처리를 위한 객체
- "작업이 끝나면 실행 시켜 줄게"라는 약속(promise)
- 비동기 작업의 완료 또는 실패를 나타내는 객체
- Promise 기반의 클라이언트가 바로 이전에 사용한 Axios 라이브러리 : 성공에 대한 약속 then(), 실패에 대한 약속 catch()

then(callback)
- 요청한 작업이 성공하면 callback 실행
- callback은 이전 작업의 성공 결과를 인자로 전달 받음

catch(callback)
- then()이 하나라도 실패하면 callback 실행
- callback은 이전 작업의 실패 객체를 인자로 전달 받음

then과 catch는 모두 항상 promise 객체를 반환
- 즉, 계속해서 chaining을 할 수 있음

axios로 처리한 비동기 로직이 항상 promise 객체를 반환

then을 계속 이어 나가면서 작성할 수 있게 됨

then 메서드 chaining의 목적
- 비동기 작업의 "순차적인" 처리 가능
- 코드를 보다 직관적이로 가독성 좋게 작성할 수 있도록 도움

then 메서드 chaining의 장점
1. 가독성
- 비동기 작업의 순서와 의존 관계를 명확히 표현할 수 있어 코드의 가독성이 향상
2. 에러 처리
- 각각의 비동기 작업 단계에서 발생하는 에러를 분할에서 처리 가능
3. 유연성
- 각 단계마다 필요한 데이터를 가공하거나 다른 비동기 작업을 수행할 수 있어서 더 복잡한 비동기 흐름을 구성할 수 있음
4. 코드 관리
- 비동기 작업을 분리하여 구성하면 코드를 관리하기 용이

Promise가 보장하는 것(vs 비동기 콜백)
1. 콜백 함수는 JavaScript의 Event Loop가 현재 실행 중인 Call Stack을 완료하기 이전에는 절대 호출되지 않음
- 반면 Promise callback 함수는 Event Queue에 배치되는 엄격한 순서로 호출됨
2. 비동기 작업이 성공하거나 실패한 뒤에 .then() 메서드를 이용하여 추가한 경우에도 호출 순서를 보장하며 동작
3. .then()을 여러 번 사용하여 여러 개의 callback 함수를 추가할 수 있음
- 각각의 callback은 주어진 순서대로 하나하나 실행하게 됨
- Chaining은 Promise의 가장 뛰어난 장점

Ajax를 활용한 클라이언트 서버 간 동작

이벤트 발생(클라이언트) -> XML 객체 생성 및 요청(클라이언트) -> Ajax 요청 처리(서버) -> 응답 데이터 생성(서버) -> JSON 데이터 응답(서버) -> 응답 데이터를 활용해 DOM 조작(웹 페이지의 일부분만을 다시 로딩)(클라이언트)

'data-*' 속성 : 사용자 지정 데이터 특성을 만들어 임의의 데이터를 HTML과 DOM 사이에서 교환 할 수 있는 방법

모든 사용자 지정 데이터는 JavaScript에서 dataset 속성을 통해 사용

주의사항
1. 대소문자 여부에 상관없이 'xml' 문자로 시작 불가
2. 세미콜론 포함 불가
3. 대문자 포함 불가

Ajax 좋아요 적용 시 유의사항
- Ajax 적용은 팔로우와 모두 동일
- 단, 팔로우와 달리 좋아요 버튼은 한 페이지에 여러 개가 존재
1. forEach()
2. querySelectorAll()




