Web 
---

World Wide Web : 인터넷으로 연결된 컴퓨터들이 정보를 공유하는 거대한 정보 공간

Web : Web site, Web application 등을 통해 사용자들이 정보를 검색하고 상호 작용하는 기술

Web site : 인터넷에서 여러 개의 Web page가 모인 것으로, 사용자들에게 정보나 서비스를 제공하는 공간

Web page : HTML, CSS 등의 웹 기술을 이용하여 만들어진 Web site를 구성하는 하나의 요소

Web page의 구성 요소
HTML : Structure, CSS : Styling, Javascript : Behavior

웹 구조화
---

HTML(Hyper Text Markup Language) : 웹 페이지의 의미와 구조를 정의하는 언어 

Hyper Text : 웹 페이지를 다른 페이지로 연결하는 링크
참조를 통해 사용자가 한 문서에서 다른 문서로 즉시 접근할 수 있는 텍스트

Markup Language : 태그 등을 이용하여 문서나 데이터의 구조를 명시하는 언어 (HTML, Markdown)

---

HTML 구조
---

<!DOCTYPE html> - 해당 문서가 html로 문서라는 것을 나타냄
<html></html> - 전체 페이지의 콘텐츠를 포함
<title></title> - 브라우저 탭 및 즐겨찾기 시 표시되는 제목으로 사용
<head></head> - HTML 문서에 관련된 설명, 설정 등, 사용자에게 보이지 않음
<body></body> - 페이지에 표시되는 모든 콘텐츠

Element(요소) - 하나의 요소는 여는 태그와 닫는 태그 그리고 그 안의 내용으로 구성됨
닫는 태그는 태그 이름 앞에 슬래시가 포함되며 닫는 태그가 없는 태그도 존재

Attributes(속성)

규칙 
- 속성은 요소 이름과 속성 사이에 공백이 있어야 함
- 하나 이상의 속성들이 있는 경우엔 속성 사이에 공백으로 구분함
- 속성 값은 열고 닫는 따옴표로 감싸야 함

목적
- 나타내고 싶진 않지만 추가적인 기능, 내용을 담고 싶을 때 사용
- CSS에서 해당 요소를 선택하기 위한 값으로 활용됨

---

HTML의 주요 목적 : 텍스트 구조와 의미를 제공하는 것

h1 요소는 단순히 텍스트를 크게만 만드는 것이 아닌 현재 문서의 최상위 제목이라는 의미를 부여하는 것

Heading & Paragraphs
- h1~6, p

Lists
- ol, ul, li

Emphasis & Importance
- em, strong

---

CSS(Cascading Style Sheet) : 웹 페이지의 디자인과 레이아웃을 구성하는 언어

CSS 적용 방법 : 인라인(Inline) 스타일, 내부(Internal) 스타일 시트, 외부(External) 스타일 시트

인라인(Inline) 스타일 : HTML 요소 안에 style 속성 값으로 작성
내부(Internal) 스타일 시트 : head 태그 안에 style 태그에 작성
외부(External) 스타일 시트 : 별도의 CSS 파일 생성 후 HTML link 태그를 사용해 불러오기

CSS Selectors : HTML 요소를 선택하여 스타일을 적용할 수 있도록 하는 선택자

기본 선택자
- 전체(*) 선택자 : HTML 모든 요소를 선택
- 요소(tag) 선택자 : 지정한 모든 태그를 선택
- 클래스('.'(dot)) 선택자 : 주어진 클래스 속성을 가진 모든 요소를 선택
- 아이디 선택자('#') : 주어진 아이디 속성을 가진 요소 선택, 문서에는 주어진 아이디를 가진 요소가 하나만 있어야 함

결합자
- 자손 결합자(""(space)) : 첫 번째 요소의 자손 요소들 선택 
- 자식 결합자(">") : 첫 번째 요소의 직계 자식만 선택

---

Specity(우선 순위) : 동일한 요소에 적용 가능한 같은 스타일을 두 가지 이상 작성했을 때 어떤 규칙이 적용되는지 결정하는 것

Cascade(계단식) : 동일한 우선 순위를 갖는 규칙이 적용될 때 CSS에서 마지막에 나오는 규칙이 사용됨

우선 순위가 높은 순 : Importance(!important) - Inline 스타일 - 선택자(id 선택자 > class 선택자 > 요소 선택자) - 소스 코드 순서

!important : 다른 우선 순위 규칙보다 우선하여 적용하는 키워드

how to render image in html MDN

상속 되는 속성
- Text 관련 요소(font, color, text-align), opacity, visibility 등

상속 되지 않는 속성
- Box model 관련 요소(width, length, border, box-sizing) 등
- Position 관련 요소(position, top/right/bottom/left, z-index) 등

---

CSS Box Model : 모든 HTML 요소를 사각형 박스로 표현하는 개념

CSS Box Model 구성 요소 : 내용(content), 안쪽 여백(padding), 테두리(border), 외부 간격(margin)으로 구성되는 개념

Content : 콘텐츠가 표시되는 영역
Padding : 콘텐츠 주위에 위치하는 공백 영역
Border : 콘텐츠와 패딩을 감싸는 테두리 영역
Margin : 이 박스와 다른 요소 사이의 공백 가장 바깥쪽 영역

width & height 속성 : 요소의 너비와 높이를 지정, 이 때 지정되는 요소의 너비와 높이는 콘텐츠 영역을 대상으로 함

CSS가 width 값을 계산하는 기준 : CSS는 border가 아닌 content의 크기를 width 값으로 지정

Normal flow : CSS를 적용하지 않았을 경우 웹 페이지 요소가 기본적으로 배치되는 방향

block 타입 특징
- 항상 새로운 행으로 나뉨
- width와 height 속성을 사용하여 너비와 높이를 지정할 수 있음
- 기본적으로 width 속성을 지정하지 않으면 박스는 inline 방향으로 사용 가능한 공간을 모두 차지함(너비를 사용 가능한 공간의 100%로 채우는 것)
- 대표적인 block 타입 태그(h1~6, p, div)

inline 타입 특징
- 새로운 행으로 나뉘지 않음
- width와 height 속성을 사용할 수 없음
- 수직 방향(padding, margins, borders가 적용되지만 다른 요소를 밀어낼 수는 없음)
- 수평 방향(padding, margins, borders가 적용되어 다른 요소를 밀어낼 수 있음)
- 대표적인 inline 타입 태그(a, img, span)

기타 display 속성

inline-block
- inline과 block 요소 사이의 중간 지점을 제공하는 display 값
- block 요소의 특징을 가짐(width 및 height 속성 사용 가능, padding, margin 및 border로 인해 다른 요소가 밀려남)
- 요소가 줄 바꿈 되는 것을 원하지 않으면서 너비와 높이를 적용하고 싶은 경우에 사용

none : 요소를 화면에 표시하지 않고, 공간조차 부여되지 않음

CSS Layout : 각 요소의 위치와 크기를 조정하여 웹 페이지의 디자인을 결정하는 것(Display, Position, Float, Flexbox 등)

CSS Position : 요소를 Normal Flow에서 제거하여 다른 위치로 배치하는 것(다른 요소 위에 올리기, 화면의 특정 위치에 고정시키기 등)

Position 유형
- static : 기본값, 요소를 Normal Flow에 따라 배치
- relative : 요소를 Normal Flow에 따라 배치, 자기 자신을 기준으로 이동, 요소가 차지하는 공간은 static일 때와 같음
- absolute : 요소를 Normal Flow에서 제거, 가장 가까운 relative 부모 요소를 기준으로 이동, 문서에서 요소가 차지하는 공간이 없어짐
- fixed : Normal Flow에서 제거, 현재 화면 영역(viewport)을 기준으로 이동, 문서에서 요소가 차지하는 공간이 없어짐
- sticky : 요소를 Normal Flow에 따라 배치, 요소가 일반적인 문서 흐름에 따라 배치되다가 스크롤이 특정 임계점에 도달하면 그 위치에서 고정됨(fixed), 만약 다음 요소가 나오면 다음 sticky 요소가 이전 sticky 요소의 자리를 대체(이전 sticky 요소가 고정되어 있던 위치와 다음 sticky 요소가 고정되어야 할 위치가 겹치게 되기 때문)

z-index : 요소가 겹쳤을 때 어떤 요소 순으로 위에 나타낼 지 결정

z-index의 특징 
- 정수 값을 사용해 Z축 순서를 지정
- 더 큰 값을 가진 요소가 작은 값의 요소를 덮음

CSS Flexbox : 요소를 행과 열 형태로 배치하는 1차원 레이아웃 방식(공간 배열 & 정렬)

Flexbox 기본 사항
- main axis(주 축) : flex item들이 배치되는 기본 축, main start에서 시작하여 main end 방향으로 배치
- cross axis(교차 축) : main axis에 수직인 축, cross start에서 시작하여 cross end 방향으로 배치
- Flex Container : display: flex; 혹은 display: inline-flex;가 설정된 부모 요소, 이 컨테이너의 1차 자식 요소들이 Flex Item이 됨, flexbox 속성 값들을 사용하여 자식 요소 Flex Item들을 배치
- Flex Item : Flex Container 내부에 레이아웃 되는 항목

Flex Container 지정
- flex item은 기본적으로 행으로 나열
- flex item은 주축의 시작 선에서 시작
- flex item은 교차축의 크기를 채우기 위해 늘어남

flex-direction 지정
- flex item이 나열되는 방향을 지정
- column으로 지정할 경우 주 축이 변경됨
- -reverse로 지정하면 시작 선과 끝 선이 서로 바뀜

flex-wrap : flex item 목록이 flex container의 하나의 행에 들어가지 않을 경우 다른 행에 배치할지 여부 설정

justify-content : 주 축을 따라 flex item과 주위에 공간을 분배

align-content
- 교차 축을 따라 flex item과 주위에 공간을 분배
flex-wrap이 wrap 또는 wrap-reverse로 설정된 여러 행에만 적용됨 
한 줄 짜리 행에는(flex-wrap이 nowrap으로 설정된 경우) 효과 없음

align-items : 교차 축을 따라 flex item 행을 정렬

align-self : 교차 축을 따라 flex item을 정렬

Flexbox 속성
Flex Container 관련 속성 - display, flex-direction, flex-wrap, justify-content, align-items, align-content
Flex Item 관련 속성 - align-self, flex-grow, flex-basis, order

목적에 따른 분류
- 배치 : flex-direction, flex-wrap
- 공간 분배 : justify-content, align-content
- 정렬 : align-items, align-self

속성명 Tip - justify : 주축, align : 교차 축

flex-grow : 남는 행 여백을 비율에 따라 각 flex item에 분배(아이템이 컨테이너 내에서 확장하는 비율을 지정), flex-grow의 반대는 flex-shrink

flex-basis
- flex item의 초기 크기 값을 지정
- flex-basis와 width 값을 동시에 적용한 경우 flex-basis가 우선

반응형 레이아웃 : 다양한 디바이스와 화면 크기에 자동으로 적응하여 콘텐츠를 최적으로 표시하는 웹 레이아웃 방식(flex-wrap을 사용해 반응형 레이아웃 작성)

shorthand 속성 - 'border' : border-width, border-style, border-color를 한 번에 설정하기 위한 속성

shorthand 속성 - 'margin', 'padding' : 4방향의 속성을 각각 지정하지 않고 한 번에 지정할 수 있는 속성

Margin collapsing(마진 상쇄) 
- 두 block 타입 요소의 martin top과 bottom이 만나 더 큰 margin으로 결합되는 현상
- 웹 개발자가 레이아웃을 더욱 쉽게 관리할 수 있도록 함(각 요소에 대한 상/하 margin을 각각 설정하지 않고 한 요소에 대해서만 설정하기 위함)

Position의 역할 : 전체 페이지에 대한 레이아웃을 구성하는 것이 아닌 페이지의 특정 항목의 위치를 조정하는 것에 관한 것

justify-items 및 justify-self 속성이 없는 이유 : margin auto를 통해 정렬 및 배치가 가능

---

Bootstrap : CSS 프론트엔드 프레임워크(Toolkit)
- 미리 만들어진 다양한 디자인 요소들을 제공하여 웹 사이트를 빠르고 쉽세 개발할 수 있도록 함

Bootstrap 기본 사용법 - mt-5 : {property}{sides}-{size}

Property
- m : margin
- p : padding

Sides
- t : top
- b : bottom
- s : left
- e : right
- y : top, bottom
- x : left, right
- blank : 4 sides

Size
- 0 : 0rem, 0px
- 1 : 0.25rem, 4px
- 2 : 0.5rem, 8px
- 3 : 1rem, 16px
- 4 : 1.5rem, 24px
- 5 : 3rem, 48px
- auto : auto, auto

Bootstrap에는 특정한 규칙이 있는 클래스 이름으로 이미 스타일 및 레이아웃이 작성되어 있음

Typography : 제목, 본문 텍스트, 목록 등

Display headings : 기존 Heading보다 더 눈에 띄는 제목이 필요한 경우(더 크고 약간 다른 스타일)
Inline text elements : HTML inline 요소에 대한 스타일
Lists : HTML list 요소에 대한 스타일

Bootstrap Color system : Bootstrap이 지정하고 제공하는 색상 시스템

Colors : Text, Border, Background 및 다양한 요소에 사용하는 Bootstrap의 색상 키워드

Bootstrap Component : Bootstrap에서 제공하는 UI 관련 요소 - 버튼, 네비게이션 바, 카드 폼, 드롭다운 등

Component : Alerts, Badges, Buttons, Cards, Navbar

Component 이점 : 일관된 디자인을 제공하여 웹 사이트의 구성 요소를 구축하는데 유용하게 활용

Semantic Web : 웹 데이터를 의미론적으로 구조화된 형태로 표현하는 방식

HTML Semantic Element : 기본적인 모양과 기능 이외에 의미를 가지는 HTML 요소 - 검색 엔진 및 개발자가 웹 페이지 콘텐츠를 이해하기 쉽도록

Semantic Element : header, nav, main, article, section, aside, footer

OOCSS(Object Oriented CSS) : 객체 지향적 접근법을 적용하여 CSS를 구성하는 방법론

CSS 방법론 : CSS를 효율적이고 유지 보수가 용이하게 작성하기 위한 일련의 가이드 라인

OOCSS 기본 원칙
- 구조와 스킨을 분리, 컨테이너와 콘텐츠를 분리

구조와 스킨을 분리
- 구조와 스킨을 분리함으로써 재사용 가능성을 높임
- 모든 버튼의 공통 구조를 정의 + 각각의 스킨(배경색과 폰트 색상)을 정의

컨테이너와 콘텐츠를 분리
- 객체에 직접 적용하는 대신 객체를 둘러싸는 컨테이너에 스타일을 적용
- 스타일을 정의할 때 위치에 의존적인 스타일을 사용하지 않도록 함
- 콘텐츠를 다른 컨테이너로 이동시키거나 재배치할 때 스타일이 깨지는 것을 방지

OOCSS 기본 원칙 : .header와 .footer 클래스가 폰트 크기와 색 둘 다 영향을 줌 
- .container .titled이 폰트 크기 담당(콘텐츠 스타일)
- .header와 .footer가 폰트 색 담당(컨테이너 스타일)

CDN(Content Delivery Network) : 지리적 제약 없이 빠르고 안전하게 콘텐츠를 전송할 수 있는 전송 기술
- 서버와 사용자 사이의 물리적인 거리를 줄여 콘텐츠 로딩에 소요되는 시간을 최소화(웹 페이지 로드 속도를 높임)
- 지리적으로 사용자와 가까운 CDN 서버에 콘텐츠를 저장해서 사용자에게 전달

Bootstrap을 사용하는 이유
- 가장 인기 있고 잘 정립된 CSS 프레임워크
- 사전에 디자인된 다양한 컴포넌트 및 기능 : 빠른 개발과 유지 보수
- 손쉬운 반응형 웹 디자인 구현
- 커스터마이징(customizing)이 용이
- 크로스 브라우징(Cross browsing) 지원 : 모든 주요 브라우저에서 작동하도록 설계되어 있음

HTML : 콘텐츠의 구조와 의미 
CSS : 레이아웃과 디자인

의미론적인 마크업의 이점
- 검색 엔진 최적화(SEO) : 검색 엔진이 해당 웹 사이트를 분석하기 쉽게 만들어 검색 순위에 영향을 줌
- 웹 접근성(Web Accessibility) : 시각 장애 사용자가 스크린 리더기로 웹 페이지를 사용할 때 추가적으로 도움

---

Bootstrap Grid system : 웹 페이지의 레이아웃을 조정하는데 사용되는 12개의 컬럼으로 구성된 시스템

Grid system 목적 : 반응형 디자인을 지원해 웹 페이지를 모바일, 태블릿, 데스크탑 등 다양한 기기에서 적절하게 표시할 수 있도록 도움

Grid system 기본 요소 
- Container : Column들을 담고 있는 공간
- Column : 실제 컨텐츠를 포함하는 부분
- Gutter : 컬럼과 컬럼 사이의 여백 영역

1개의 row 안에 12칸의 column 영역이 구성, 각 요소는 12칸 중 몇 개를 차지할 것인지 지정됨

Gutters : Grid system에서 column 사이에 여백 영역(x축은 padding, y축은 margin으로 여백 생성)

Responsive Web Design : 디바이스 종류나 화면 크기에 상관 없이, 어디서든 일관된 레이아웃 및 사용자 경험을 제공하는 디자인 기술

Bootstrap Grid system에서는 12개 column과 6개 breakpoints를 사용하여 반응형 웹 디자인을 구현

Grid system breakpoints : 웹 페이지를 다양한 화면 크기에서 적절하게 배치하기 위한 분기점
- 화면 너비에 따라 6개의 분기점 제공(xs, sm, md, lg, xl, xxl)

각 breakpoints마다 설정된 최대 너비 값 "이상으로" 화면이 커지면 grid system 동작이 변경됨

Grid system은 화면 크기에 따라 12개의 칸을 각 요소에 나누어 주는 것

The Grid system 
- CSS가 아닌 편집 디자인에서 나온 개념으로 구성 요소를 잘 배치해서 시각적으로 좋은 결과물을 만들기 위함
- 기본적으로 안쪽에 있는 요소들의 오와 열을 맞추는 것에서 기인
- 정보 구조와 배열을 체계적으로 작성하여 정보의 질서를 부여하는 시스템

Grid cards : row-cols 클래스를 사용하여 행당 표시할 열(카드) 수를 손쉽게 제어할 수 있음