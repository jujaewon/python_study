Django
---

Django : Python 기반의 대표적인 웹 프레임 워크

Framework : 웹 애플리케이션을 빠르게 개발할 수 있도록 도와주는 도구(개발에 필요한 기본 구조, 규칙, 라이브러리 등을 제공)

Client : 서비스를 요청하는 주체(웹 사용자의 인터넷이 연결된 장치, 웹 브라우저)

Server : 클라이언트의 요청에 응답하는 주체(웹 페이지, 앱을 저장하는 컴퓨터)

가상 환경 : Python 애플리케이션과 그에 따른 패키지들을 격리하여 관리할 수 있는 독립적인 실행 환경

가상 환경이 필요한 시나리오 : 다른 패키지 버전을 사용, 패키지 충돌을 피하기

가상 환경 venv 생성 : $ python -m venv venv (venv라는 이름의 가상 환경 만들기)

가상 환경 활성화 : $ source venv/Scripts/activate

환경에 설치된 패키지 목록 확인 : $ pip list

패키지 목록이 필요한 시나리오 : 어떤 패키지를 설치했고 어떤 버전을 설치했는지 알아야 할 때

의존성 패키지 

- 한 소프트웨어 패키지가 다른 패키지의 기능이나 코드를 사용하기 때문에 그 패키지가 존재해야만 제대로 작동하는 관계

- 사용하려는 패키지가 설치되지 않았거나, 호환되는 버전이 아니면 오류가 발생하거나 예상치 못한 동작을 보일 수 있음

의존성 패키지 관리의 중요성 : 개발 환경에서는 각각의 프로젝트가 사용하는 패키지와 그 버전을 정확히 관리하는 것이 중요

의존성 패키지 목록 생성 : $ pip freeze > requirements.txt

Django 프로젝트 생성 전 루틴 : 가상 환경 생성 -> 가상 환경 활성화 -> Django 설치 -> 의존성 파일 생성(패키지 설치시마다 진행)

Django 프로젝트 생성 : $ django-admin startproject firstpjt .(firstpjt라는 이름의 프로젝트를 생성)

Django 서버 실행 : $ python manage.py runserver(manage.py와 동일한 경로에서 명령어 진행)

Django 프로젝트 생성 전 루틴 정리 + git : 가상 환경 생성 -> 가상 환경 활성화 -> Django 설치 -> 의존성 파일 생성(패키지 설치시마다 진행) -> .gitignore 파일 생성(첫 add전) -> git 저장소 생성 -> Django 프로젝트 생성

가상 환경을 사용하는 이유

- 의존성 관리 : 라이브러리 및 패키지를 각 프로젝트마다 독립적으로 사용 가을
- 팀 프로젝트 협업 : 모든 팀원이 동일한 환경과 의존성 위에서 작업하여 버전간 충돌을 방지

LTS(Long-Term Support)

- 프레임워크나 라이브러리 등의 소프트웨어에서 장기간 지원되는 안정적인 버전을 의미할 때 사용
- 기업이나 대규모 프로젝트에서는 소프트웨어 업그레이드에 많은 비용과 시간이 필요하기 때문에 안정적이고 장기간 지원되는 버전이 필요

Django project : 애플리케이션의 집합(DB 설정, URL 연결, 전체 앱 설정 등을 처리)

Django application : 독립적으로 작동하는 기능 단위 모듈(각자 특정한 기능을 담당하며 다른 앱들과 함께 하나의 프로젝트를 구성)

앱 사용 과정 : 앱 생성 -> 앱 등록

앱 생성(앱의 이름은 '복수형'으로 지정하는 것을 권장) : $ python manage.py startapp articles

앱 등록(반드시 앱을 생성한 후에 등록해야 함, 등록 후 생성은 불가능)

디자인 패턴 : 소프트웨어 설계에서 발생하는 문제를 해결하기 위한 일반적인 해결책(공통적인 문제를 해결하는데 쓰이는 형식화 된 관행)

MVC 디자인 패턴(Model, View, Controller) : 애플리케이션을 구조화하는 대표적인 패턴(데이터, 사용자 인터페이스, 비즈니스 로직을 분리) - 시각적 요소와 뒤에서 실행되는 로직을 서로 영향 없이, 독립적이고 쉽게 유지 보수할 수 있는 애플리케이션을 만들기 위해

MTV 디자인 패턴(Model, Template, View) : Django에서 애플리케이션을 구조화하는 패턴(기존 MVC 패턴과 동일하나 명칭을 다르게 정의한 것)

프로젝트 구조
- settings.py : 프로젝트의 모든 설정을 관리
- urls.py : URL과 이에 해당하는 적절한 views를 연결
(아래는 수정할 일 없음)
- __init__.py : 해당 폴더를 패키지로 인식하도록 설정
- asgi.py : 비동기식 웹 서버와의 연결 관련 설정
- wsgi.py : 웹 서버와의 연결 관련 설정
- manage.py : Django 프로젝트와 다양한 방법으로 상호작용하는 커맨드라인 유틸리티

앱 구조
- admin.py : 관리자용 페이지 설정
- models.py : DB와 관련된 Model을 정의, MTV 패턴의 M
- views.py : HTTP 요청을 처리하고 해당 요청에 대한 응답을 반환(url, mode, template과 연계), MTV 패턴의 V
(아래는 수정할 일 없음)
- apps.py : 앱의 정보가 작성된 곳
- tests.py : 프로젝트 테스트 코드를 작성하는 곳

URLS - http://127.0.0.1:8000/articles/로 요청이 왔을 때 views 모듈의 index 뷰 함수를 호출

from articles import views : articles 패키지에서 views 모듈을 가져오는 것
url 경로는 반드시 '/'(slash)로 끝나야 함

View : 특정 경로에 있는 template과 request 객체를 결합해 응답 객체를 반환하는 index view 함수 정의(모든 view 함수는 첫 번째 인자로 request(요청) 객체를 필수적으로 받음)

Template(폴더명은 반드시 templates여야 하며 개발자가 직접 생성해야 함)
- articles 앱 폴더 안에 templates 폴더 생성
- templates 폴더 안에 articles 폴더 생성
- articles 폴더 안에 템플릿 파일 생성

Django에서 template을 인식하는 경로 규칙
- app폴더 / templates / articles / index.html
- app폴더 / templates / example.html

Django는 templates / 지점까지 기본 경로로 인식하기 때문에 이후의 template 경로를 작성해야 함

데이터 흐름에 따른 코드 작성 : URLs -> View -> Template

MTV 디자인 패턴 정리

Model
- 데이터와 관련된 로직을 정리
- 응용 프로그램의 데이터 구조를 정의하고 데이터베이스의 기록을 관리

Template
- 레이아웃과 화면을 처리
- 화면상의 사용자 인터페이스 구조와 레이아웃을 정의

View
- Model & Template과 관련한 로직을 처리해서 응답을 반환
- 클라이언트의 요청에 대해 처리를 분기하는 역할

View 예시 
- 데이터가 필요하다면 model에 접근해서 데이터를 가져오고
- 가져온 데이터를 template로 보내 화면을 구성하고,
- 구성된 화면을 응답으로 만들어 클라이언트에게 반환

render 함수 : 주어진 템플릿을 주어진 컨텍스트 데이터와 결합하고 렌더링 된 텍스트와 함께 HttpResponse(응답) 객체를 반환하는 함수

request : 응답을 생성하는 데 사용되는 요청 객체

template_name : 템플릿 이름의 경로

context : 템플릿에서 사용할 데이터(딕셔너리 타입으로 작성)

Django Template system : 데이터 표현을 제어하면서 표현과 관련된 부분을 담당

Django Template Language(DTL) : Template에서 조건, 반복, 변수 등의 프로그래밍적 기능을 제공하는 시스템

DTL Syntax

Variable 
- render 함수의 세 번째 인자로 딕셔너리 데이터를 사용
- 딕셔너리 key에 해당하는 문자열이 template에서 사용 가능한 변수명이 됨
- dot(.)를 사용하여 변수 속성에 접근할 수 있음

Filters
- 표시할 변수를 수정할 때 사용
- chained가 가능하며 일부 필터는 인자를 받기도 함
- 약 60개의 built-in template filters를 제공

Tags 
- 반복 또는 논리를 수행하여 제어 흐름을 만듦
- 일부 태그는 시작과 종료 태그가 필요
- 약 24개의 built-in template tags를 제공

Comments : {% comment %} {% endcomment %}

템플릿 상속(Template inheritance) : 페이지의 공통요소를 포함하고, 하위 템플릿이 재정의 할 수 있는 공간을 정의하는 기본 'skeleton' 템플릿을 작성하여 상속 구조를 구축

'extends' tag({% extends 'path' %}) : 자식(하위) 템플릿이 부모 템플릿을 확장한다는 것을 알림(반드시 템플릿 최상단에 작성되어야 함(2개 이상 사용 불가))

'extends' tag({% block name %} {% endblock name %}) : 하위 템플릿에서 재정의 할 수 있는 블록을 정의(하위 템플릿이 작성할 수 있는 공간을 지정)

데이터를 보내고 가져오기(Sending and Retrieving form data) : HTML form element를 통해 사용자와 애플리케이션 간의 상호 작용 이해하기

HTML form은 HTTP 요청을 서버에 보내는 가장 편리한 방법

'form' element : 사용자로부터 할당된 데이터를 서버로 전송 
- 웹에서 사용자 정보를 입력하는 여러 방식(text, password, checkbox 등)을 제공

action, method : 데이터를 어디(action)로 어떤 방식(method)으로 요청할지

action
- 입력 데이터가 전송될 URL을 지정(목적지)
- 만약 이 속성을 지정하지 않으면 데이터는 현재 form이 있는 페이지의 URL로 보내짐

method
- 데이터를 어떤 방식으로 보낼 것인지 정의
- 데이터의 HTTP request methods(GET, POST)를 지정

'input' element : 사용자의 데이터를 입력 받을 수 있는 요소(type 속성 값에 따라 다양한 유형의 입력 데이터를 받음)

'name' attribute(input의 핵심 속성) : 입력한 데이터에 붙이는 이름(key)
- 데이터를 제출했을 때 서버는 name 속성에 설정된 값을 통해서만 사용자가 입력한 데이터에 접근할 수 있음

Query String Parameters
- 사용자의 입력 데이터를 URL 주소에 파라미터를 통해 서버로 보내는 방법
- 문자열은 앰퍼샌드(&)로 연결된 key=value 쌍으로 구성되며, 기본 URL과 물음표(?)로 구분됨

HTTP request 객체 : form으로 전송한 데이터 뿐만 아니라 모든 요청 관련 데이터가 담겨 있음(view 함수의 첫번째 인자)

URL dispatcher(운항 관리자, 분배기) : URL 패턴을 정의하고 해당 패턴이 일치하는 요청을 처리할 view 함수를 연결(매핑)

Variable Routing : URL 일부에 변수를 포함시키는 것(변수는 view 함수의 인자로 전달 할 수 있음)

Variable Routing 작성법 : <path_converter:variable_name>

Path converters : URL 변수의 타입을 지정(str, int 등 5가지 타입 지원)

App URL mapping : 각 앱에 URL을 정의하는 것 
- 프로젝트와 각 앱이 URL을 나누어 관리를 편하게 하기 위함

include() : 프로젝트 내부 앱들의 URL을 참조할 수 있도록 매핑하는 함수
- URL의 일치하는 부분까지 잘라내고, 남은 문자열 부분은 후속 처리를 위해 include된 URL로 전달

Naming URL patterns : URL에 이름을 지정하는 것(path 함수의 name 인자를 정의해서 사용)

Naming URL patterns 적용 : path 함수의 name 키워드 인자를 정의해서 사용

URL 표기 변화 : href 속성 값 뿐만 아니라 form의 action 속성처럼 url을 작성하는 모든 위치에서 변경

'url' tag({% url 'url-name' arg1 arg2 %}) : 주어진 URL 패턴의 이름과 일치하는 절대 경로 주소를 반환

Django Model : DB의 테이블을 정의하고 데이터를 조작할 수 있는 기능들을 제공 - 테이블 구조를 설계하는 청사진

django.db.models 모듈의 Model이라는 부모 클래스를 상속 받음

model 클래스 : 

class Article(models.Model):
    title = models.CharField()
    content = models.TextField()

Model은 model에 관련된 모든 코드가 이미 작성되어있는 클래스

클래스 변수명 - 테이블의 각 필드(열) 이름

model Field 클래스 : 테이블 필드의 데이터 타입 

model Field 클래스의 키워드 인자(필드 옵션) : 테이블 필드의 제약조건 관련 설정

제약 조건 : 데이터가 올바르게 저장되고 관리되도록 하기 위한 규칙

Migrations : Model 클래스의 변경 사항(필드 생성, 수정 삭제 등)을 DB에 최종 반영하는 방법

Migrations 핵심 명령어 2가지
- $ python manage.py makemigrations : model class를 기반으로 최종 설계도(migration) 작성
- $ python manage.py migrate : 최종 설계도를 DB에 전달하여 반영

추가 모델 필드 작성 :
class Article(models.Model):
    title = models.CharField(max_length=10)
    content = models.TextField()
    created_at = models.DateTimeField(auto_now_add=True)
    updated_at = models.DateTimeField(auto_now=True)

이미 기존 테이블이 존재하기 때문에 필드를 추가할 때 필드의 기본 값 설정이 필요

model class에 변경 사항이 생겼다면, 반드시 새로운 설계도를 생성하고 이를 DB에 반영해야 한다.

model class 변경 -> makemigrations -> migrate

Model Field : DB 테이블의 필드(열)을 정의하며, 해당 필드에 저장되는 데이터 타입과 제약 조건을 정의

CharField() : 길이의 제한이 있는 문자열을 넣을 때 사용(필드의 최대 길이를 결정하는 max_length는 필수 인자)

TextField() : 글자의 수가 많을 때 사용

DateTimeField() : 날짜와 시간을 넣을 때 사용

DateTimeField의 선택 인자
- auto_now : 데이터가 저장될 때마다 자동으로 현재 날짜 시간을 저장
- auto_now_add : 데이터가 처음 생성될 때만 자동으로 현재 날짜 시간을 저장

Automatic admin interface 
- Django는 추가 설치 및 설정 없이 자동으로 관리자 인터페이스를 제공 : 데이터 확인 및 테스트 등을 진행하는데 매우 유용

admin 계정 생성 : $ python manage.py createsuperuser

admin에 모델 클래스 등록 : admin.py에 작성한 모델 클래스를 등록해야만 admin site에서 확인 가능

데이터베이스 초기화 
migration 파일 삭제 -> db.sqlite3 파일 삭제
(__init__.py 파일과, migrations 폴더를 지우지 않도록 주의)

Migrations 기타 명령어

$ python manage.py showmigrations
- migrations 파일들이 migrate 됐는지 안됐는지 여부를 확인하는 명령어
- [X] 표시가 있으면 migrate가 완료되었음을 의미

$ python manage.py sqlmigrate articles 0001
- 해당 migrations 파일이 SQL 언어(DB에서 사용하는 언어)로 어떻게 번역되어 DB에 전달되는지 확인하는 명령어

첫 migrate시 출력 내용이 많은 이유 : Django 프로젝트가 동작하기 위해 미리 작성되어있는 기본 내장 app들에 대한 migration 파일들이 함께 migrate되기 때문

CRUD : 소프트웨어가 가지는 기본적인 데이터 처리 기능
Create(저장), Read(조회), Update(갱신), Delete(삭제)

ORM(Object-Relational-Mapping) : 객체 지향 프로그래밍 언어를 사용하여 호환되지 않는 유형의 시스템 간에 데이터를 변환하는 기술

QuerySet API : ORM에서 데이터를 검색, 필터링, 정렬 및 그룹화하는데 사용하는 도구 - API를 사용하여 SQL이 아닌 Python 코드로 데이터를 처리

QuerySet API 구문 : Model class.Manager.Queryset API

Query

- 데이터베이스에 특정한 데이터를 보여 달라는 요청
- "쿼리문을 작성한다." : 원하는 데이터를 얻기 위해 데이터베이스에 요청을 보낼 코드를 작성한다.
- 파이썬으로 작성한 코드가 ORM에 의해 SQL로 변환되어 데이터베이스에 전달되며, 데이터베이스의 응답 데이터를 ORM이 QuerySet이라는 자료 형태로 변환하여 우리에게 전달

QuerySet

- 데이터베이스에게서 전달 받은 객체 목록(데이터 모음) : 순회가 가능한 데이터로써 1개 이상의 데이터를 불러와 사용할 수 있음
- Django ORM을 통해 만들어진 자료형
- 단, 데이터베이스가 단일한 객체를 반환할 때는 QuerySet이 아닌 모델(Class)의 인스턴스로 반환됨

Python의 모델 클래스와 인스턴스를 활용해 DB에 데이터를 저장, 조회, 수정, 삭제하는 것

외부 라이브러리 설치 및 설정
- pip install ipython -> pip install django-extensions -> pip freeze > requirements.txt

Django shell : Django 환경 안에서 실행되는 python shell(입력하는  QuerySet API 구문이 Django 프로젝트에 영향을 미침)

Django shell 실행 : python manage.py shell_plus

save() : 객체를 데이터베이스에 저장하는 메서드

all() : 전체 데이터 조회

get() : 단일 데이터 조회

get() 특징 : 객체를 찾을 수 없으면 DoesNotExist 예외를 발생시키고, 둘 이상의 객체를 찾으면 MultipleObjectsReturned 예외를 발생시킴

- 위와 같은 특징을 가지고 있기 때문에 primary key와 같이 고유성(uniqueness)을 보장하는 조회에서 사용해야 함

filter() : 특정 조건 데이터 조회

데이터 수정 : 인스턴스 변수를 변경 후 save 메서드 호출

데이터 삭제 : 삭제하려는 데이터 조회 후 delete 메서드 호출

Field lookups : 특정 레코드에 대한 조건을 설정하는 방법(QuerySet 메섣, filter(), exclude() 및 get()에 대한 키워드 인자로 지정됨)

ORM, QuerySet API를 사용하는 이유

- 데이터베이스 쿼리를 추상화하여 Django 개발자가 데이터베이스와 직접 상호작용하지 않아도 되도록 함
- 데이터베이스와의 결합도를 낮추고 개발자가 더욱 직관적이고 생산적으로 개발할 수 있도록 도움

Create 로직을 구현하기 위해 필요한 view 함수의 개수는 2개

- 사용자 입력 데이터를 받을 페이지를 렌더링 : new
- 사용자가 입력한 데이터를 받아 DB에 저장 : create

HTTP : 네트워크 상에서 데이터를 주고 받기위한 약속

HTTP request methods : 데이터(리소스)에 어떤 요청(행동)을 원하는지를 나타내는 것 - GET & POST

GET Method : 특정 리소스를 조회하는 요청(GET으로 데이터를 전달하면 Query String 형식으로 보내짐)
POST Method : 특정 리소스에 변경(생성, 수정, 삭제)을 요구하는 요청(POST로 데이터를 전달하면 HTTP Body에 담겨 보내짐)

HTTP response status code : 특정 HTTP 요청이 성공적으로 완료되었는지를 3자리 숫자로 표현하기로 약속한 것

403 Forbidden : 서버에 요청이 전달되었지만, 권한 때문에 거절되었다는 것을 의미

CSRF(Cross-Site-Request-Forgery)

사이트 간 요청 위조 : 사용자가 자신의 의지와 무관하게 공격자가 의도한 행동을 하여 특정 웹 페이지를 보안에 취약하게 하거나 수정, 삭제 등의 작업을 하게 만드는 공격 방법

CSRF Token 적용
- DTL의 csrf_token 태그를 사용해 사용자에게 토큰 값을 부여
- 요청 시 토큰 값도 함께 서버로 전송될 수 있도록 함

요청 시 CSRF Token을 함께 보내야 하는 이유
- Django 서버는 해당 요청이 DB에 데이터를 하나 생성하는(DB에 영향을 주는) 요청에 대해 "Django가 직접 제공한 페이지에서 데이터를 작성하고 있는 것 인지"에 대한 확인 수단이 필요한 것

POST일 때만 Token을 확인하는 이유 : POST는 단순 조회를 위한 GET과 달리 특정 리소스에 변경(생성, 수정, 삭제)을 요구하는 의미와 기술적인 부분을 가지고 있기 때문

- DB에 조작을 가하는 요청은 반드시 인증 수단이 필요
- 데이터베이스에 대한 변경사항을 만드는 요청이기 때문에 토큰을 사용해 최소한의 신원 확인을 하는 것

redirect() : 클라이언트가 인자에 작성된 주소로 다시 요청을 보내도록 하는 함수

redirect 특징
- 해당 redirect에서 클라이언트는 detail url로 요청을 다시 보내게 됨
- 결과적으로 detail view 함수가 호출되어 detail view 함수의 반환 결과인 detail 페이지를 응답 받음

Create 로직을 구현하기 위해 필요한 view 함수의 개수는 2개

- 사용자 입력 데이터를 받을 페이지를 렌더링 : edit
- 사용자가 입력한 데이터를 받아 DB에 저장 : update

유효성 검사 : 수집한 데이터가 정확하고 유효한지 확인하는 과정

Django Form : 사용자 입력 데이터를 수집하고, 처리 및 유효성 검사를 수행하기 위한 도구
- 유효성 검사를 단순화하고 자동화 할 수 있는 기능을 제공

Widgets : HTML 'input' element의 표현을 담당

Widgets은 단순히 input 요소의 속성 및 출력되는 부분을 변경하는 것

ModelForm : Model과 연결된 Form을 자동으로 생성해주는 기능을 제공

Meta class : ModelForm의 정보를 작성하는 곳

exclude 속성을 사용하여 모델에서 포함하지 않을 필드를 지정할 수도 있음

is_valid() : 여러 유효성 검사를 실행하고, 데이터가 유효한지 여부를 Boolean으로 반환

모델 필드에는 기본적으로 빈 값은 허용하지 않는 제약 조건이 설정되어있음
빈 값은 is_valid()에 의해 False로 평가되고 form 객체에는 그에 맞는 에러 메시지가 포함되어 다음 코드로 진행됨

save() : 데이터베이스 객체를 만들고 저장
- 키워드 인자 instance 여부를 통해 생성할 지, 수정할 지를 결정

new & create view 함수간 공통점과 차이점
- 공통점 : "데이터 생성을 구현하기 위함"
- 차이점 : "new는 GET method 요청만을, create는 POST method 요청만을 처리"

HTTP request method 차이점을 활용해 view 함수 구조 변경

Static Files(정적 파일) : 서버 측에서 변경되지 않고 고정적으로 제공되는 파일(이미지, JS, CSS 파일 등)

웹 서버의 기본 동작 : 특정 위치(URL)에 있는 자원을 요청(HTTP request) 받아서 응답(HTTP response)을 처리하고 제공(serving)하는 것
- 웹 서버는 요청 받은 URL로 서버에 존재하는 정적 자원을 제공함 : 정적 파일을 제공하기 위한 경로(URL)가 있어야 함

Static files 기본 경로 : app폴더/static/

기본 경로 static file 제공하기 
- articles/static/articles/ 경로에 이미지 파일 배치
- static tag를 사용해 이미지 파일에 대한 url 제공

STATIC_URL : 기본 경로 및 추가 경로에 위치한 정적 파일을 참조하기 위한 URL, 실제 파일이나 디렉토리가 아니며, URL로만 존재(STATIC_URL = 'static/')

URL + STATIC_URL + 정적 파일 경로

Static files 추가 경로 : STATICFILES_DIRS에 문자열 값으로 추가 경로 설정

STATICFILES_DIRS : 정적 파일의 기본 경로 외에 추가적인 경로 목록을 정의하는 리스트

임의의 추가 경로 설정 : BASE_DIR / 'static',

추가 경로 static file 제공하기 : 추가 경로에 이미지 파일 배치, static tag를 사용해 이미지 파일에 대한 url 제공 

정적 파일을 제공하려면 요청에 응답하기 위한 URL이 필요

Media Files : 사용자가 웹에서 업로드하는 정적 파일(user-uploaded)

ImageField() : 이미지 업로드에 사용하는 모델 필드 
- 이미지 객체가 직접 저장되는 것이 아닌 '이미지 파일의 경로'가 문자열로 DB에 저장

미디어 파일을 제공하기 전 준비
- settings.py에 MEDIA_ROOT, MEDIA_URL 설정
- 작성한 MEDIA_ROOT와 MEDIA_URL에 대한 url 지정

MEDIA_ROOT : 미디어 파일들이 위치하는 디렉토리의 절대 경로

MEDIA_URL : MEDIA_ROOT에서 제공되는 미디어 파일에 대한 주소를 생성(STATIC_URL과 동일한 역할)

MEDIA_ROOT와 MEDIA_URL에 대한 url 지정
- 업로드 된 파일의 URL : settings.MEDIA_URL
- 위 URL을 통해 참조하는 파일의 실제 위치 : settings.MEDIA_ROOT

이미지 업로드 
- blank=True 속성을 작성해 빈 문자열이 저장될 수 있도록 제약 조건 설정
- migration 진행
- form 요소의 enctype 속성 추가(enctype="multipart/form-data")
- view 함수에서 업로드 파일에 대한 추가 코드 작성
- 이미지 업로드 입력 양식 확인
- 이미지 업로드 결과 확인

업로드 이미지 제공하기
- 'url' 속성을 통해 업로드 파일의 경로 값을 얻을 수 있음
- article.image.url : 업로드 파일의 경로
- article.image : 업로드 파일의 파일 이름
- 업로드 이미지 출력 확인 및 MEDIA_URL 확인
- 이미지를 업로드하지 않은 게시물은 detail 템플릿을 렌더링 할 수 없음
- 이미지 데이터가 있는 경우만 이미지를 출력할 수 있도록 처리

업로드 이미지 속성 
- 수정 페이지 form 요소에 enctype 속성 추가
- update view 함수에서 업로드 파일에 대한 추가 코드 작성

upload_to argument : ImageField()의 upload_to 인자를 사용해 미디어 파일 추가 경로 설정

request.FILES가 두번째 위치 인자인 이유 : ModelForm 상위 클래스 BaseModelForm의 생성자 함수 키워드 인자




