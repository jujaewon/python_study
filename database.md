데이터베이스

데이터베이스 : 체계적인 데이터 모음

데이터 : 저장이나 처리에 효율적인 형태로 변환된 정보

기존의 데이터 저장 방식 : 파일 이용, 스프레드 시트 이용

파일을 이용한 데이터 관리 
- 어디에서나 쉽게 사용 가능
- 데이터를 구조적으로 관리하기 어려움

스프레드 시트를 이용한 데이터 관리 : 테이블의 열과 행을 사용해 데이터를 구조적으로 관리 가능

스프레드 시트의 한계
- 크기 : 일반적으로 약 100만 행까지만 저장 가능
- 보안 : 단순히 파일이나 링크 소유 여부에 따른 단순한 접근 권한 기능 제공

데이터 베이스 역할 : 데이터를 저장하고 조작

관계형 데이터베이스 : 데이터 간에 관계가 있는 데이터 항목들의 모음
- 테이블, 행, 열의 정보를 구조화하는 방식
- 서로 관련된 데이터 포인터를 저장하고 이에 대한 액세스를 제공

관계 : 여러 테이블 간의 (논리적) 연결

Table : 데이터를 기록하는 곳

Field : 각 필드에는 고유한 데이터 형식(타입)이 지정됨

Record : 각 레코드에는 구체적인 데이터 값이 저장됨

Database : 테이블의 집합

Primary Key (기본키)
- 각 레코드의 고유한 값
- 관계형 데이터베이스에서 레코드의 식별자로 활용

Foreign Key (외래 키)
- 테이블의 필드 중 다른 테이블의 레코드를 식별할 수 있는 키
- 다른 테이블의 기본 키를 참조
- 각 레코드에서 서로 다른 테이블 간의 관계를 만드는데 사용

DBMS (Relational Database Management System) : 데이터베이스를 관리하는 소프트웨어 프로그램 

RDBMS (Relational Database Management System) : 관계형 데이터베이스를 관리하는 소프트웨어 프로그램

DBMS
- 데이터 저장 및 관리를 용이하게 하는 시스템
- 데이터베이스와 사용자 간의 인터페이스 역할
- 사용자가 데이터 구성, 업데이트, 모니터링, 백업, 복구 등을 할 수 있도록 도움

RDBMS 서비스 종류 : SQLite, MySQL, PostgreSQL, Oracle Database

Table에는 행에서 고유하게 식별 가능한 기본 키라는 속성이 있으며, 외래 키를 사용하여 각 행에서 서로 다른 테이블 간의 관계를 만들 수 있음

데이터는 기본 키 또는 외래 키를 통해 결합(join)될 수 있는 여러 테이블에 걸쳐 구조화 됨

SQL (Structure Query Language) : 데이터베이스에 정보를 저장하고 처리하기 위한 프로그래밍 언어

SQL : 관계형 데이터베이스와의 대화를 위해 사용하는 프로그래밍 언어

SQL Syntax : SELECT column_name FROM table_name;

SQL 키워드는 대소문자를 구분하지 않음
- 하지만 대문자로 작성하는 것을 권장(명시적 구분)

각 SQL Statements의 끝에는 세미콜론(;)이 필요
- 세미콜론은 각 SQL Statements를 구분하는 방법(명령어의 마침표)

SQL Statements : SQL을 구성하는 가장 기본적인 코드 블록

SELECT column_name FROM table_name;
- 해당 예시 코드는 SELECT Statement라 부름
- 이 Statement는 SELECT, FROM 2개의 keyword로 구성 됨
  
수행 목적에 따른 SQL Statements 4가지 유형

DDL : 데이터의 기본 구조 및 형식 변경
DQL : 데이터 검색
DML : 데이터 조작
DCL : 데이터 및 작업에 대한 사용자 권한 제어

Query : '데이터베이스로부터 정보를 요청'하는 것
- 일반적으로 SQL로 작성하는 코드를 쿼리문(SQL문)이라 함
  
SELECT statement : 테이블에서 데이터를 조회

SELECT syntax

SELECT
  select_list
FROM
  table_name;

- SELECT 키워드 이후 데이터를 선택하려는 필드를 하나 이상 지정
- FROM 키워드 이후 데이터를 선택하려는 테이블의 이름을 지정

SELECT 문을 사용하여 테이블의 데이터를 조회 및 반환
- '*'(asterisk)를 사용하여 모든 필드 선택

ORDER BY statement : 조회 결과의 레코드르 정렬

ORDER BY syntax
- FROM clause 뒤에 위치
- 하나 이상의 컬럼을 기준으로 결과를 오름차순(ASC, 기본값), 내림차순(DESC)으로 정렬

SELECT statement 실행 순서 : FROM -> SELECT -> ORDER BY

Filtering data 관련 Keywords
- Clause : DISTINCT, WHERE, LIMIT
- Operator : BETWEEN, IN, LIKE, Comparison, Logical

DISTINCT statement : 조회 결과에서 중복된 레코드를 제거

DISTINCT syntax
- SELECT 키워드 바로 뒤에 작성해야 함
- SELECT DISTINCT 키워드 다음에 고유한 값을 선택하려는 하나 이상의 필드를 지정

WHERE statement : 조회 시 특정 검색 조건을 지정
WHERE syntax
- FROM clause 뒤에 위치
- search_condition은 비교연산자 및 논리연산자(AND, OR, NOT 등)를 사용하는 구문이 사용됨

Comparison Operators(비교 연산자)
- =, >=, <=, !=, IS, LIKE, IN, BETWEEN ... AND

Logical Operators(논리 연산자)
- AND(&&), OR(||), NOT(!)

IN Operator : 값이 특정 목록 안에 있는지 확인

LIKE Operator : 값이 특정 패턴에 일치하는지 확인(Wildcards와 함께 사용)

Wildcard Characters
- '%' : 0개 이상의 문자열과 일치하는지 확인
- '_' : 단일 문자와 일치하는지 확인

LIMIT clause : 조회하는 레코드 수를 제한

LIMIT syntax
- 하나 또는 두 개의 인자를 사용 (0또는 양의 정수)
- row_count는 조회하는 최대 레코드 수를 지정

GROUP BY clause
- 레코드를 그룹화하여 요약본 생성('집계 함수'와 함께 사용)

Aggregation Functions(집계 함수)
- 값에 대한 계산을 수행하고 단일한 값을 반환하는 함수(SUM, AVG, MAX, MIN, COUNT)

GROUP BY syntax
- FROM 및 WHERE 절 뒤에 배치
- GROUP BY 절 뒤에 그룹화 할 필드 목록을 작성

HAVING clause
- 집계 항목에 대한 세부 조건을 지정
- 주로 GROUP BY와 함께 사용되며 GROUP BY가 없다면 WHERE처럼 동작

ELECT statement 실행 순서 : FROM -> WHERE -> GROUP BY -> HAVING -> SELECT -> ORDER BY -> LIMIT

CREATE TABLE statement : 테이블 생성

CREATE TABLE table_name (
  column_1 data_type constraints,
  column_2 data_type constraints,
  ...,
);

- 각 필드에 적용할 데이터 타입 작성
- 테이블 및 필드에 대한 제약조건(constraints) 작성

SQLite 데이터 타입
1. NULL - 아무런 값도 포함하지 않음을 나타냄
2. INTEGER - 정수
3. REAL - 부동 소수점
4. TEXT - 문자열
5. BLOB - 이미지, 동영상, 문서 등의 바이너리 데이터

Constraints(제약 조건) : 테이블의 필드에 적용되는 규칙 또는 제한 사항
- 데이터의 무결성을 유지하고 데이터베이스의 일관성을 보장

PRIMARY KEY : 해당 필드를 기본 키로 지정
- INTEGER 타입에만 적용되며, INT, BIGINT등과 같은 정수 유형은 적용되지 않음

NOT NULL : 해당 필드에 NULL 값을 허용하지 않도록 지정

FOREING KEY : 다른 테이블과의 외래 키 관계를 정의

AUTOINCREMENT keyword : 자동으로 고유한 정수 값을 생성하고 할당하는 필드 속성

AUTOINCREMENT 특징
- 필드의 자동 증가를 나타내는 특수한 키워드
- 주로 primary key 필드에 적용
- INTEGER PRIMARY KEY AUTOINCREMENT가 작성된 필드는 항상 새로운 레코드에 대해 이전 최대값보다 큰 값을 할당
- 삭제된 값은 무시되며 재사용할 수 없게 됨

ALTER TABLE statement : 테이블 및 필드 조작

ADD COLUMN : 필드 추가
RENAME COLUMN : 필드 이름 변경
DROP COLUMN : 필드 삭제
RENAME TO : 테이블 이름 변경

ALTER TABLE ADD COLUMN syntax

ALTER TABLE
  table_name
ADD COLUMN
  column_definition;

- ADD COLUMN 키워드 이후 추가하고자 하는 새 필드 이름과 데이터 타입 및 제약 조건 작성

SQLite는 단일 문을 사용하여 한 번에 여러 필드를 추가할 수 없음

ALTER TABLE RENAME COLUMN syntax

ALTER TABLE
  table_name
RENAME COLUMN
  current_name TO new_name;

- RENAME COLUMN 키워드 뒤에 이름을 바꾸려는 필드의 이름을 지정하고 TO 키워드 뒤에 새 이름을 지정

ALTER TABLE DROP COLUMN syntax

ALTER TABLE
  table_name
DROP COLUMN
  current_name

- DROP COLUMN 키워드 뒤에 삭제하려는 필드의 이름을 지정
- 삭제하는 필드가 다른 부분에서 참조되지 않고 PRIMARY KEY가 아니며 UNIQUE 제약 조건이 없는 경우에만 작동

ALTER TABLE RENAME TO syntax

ALTER TABLE
  table_name
RENAME COLUMN
  new_table_name


DROP TABLE statement : 테이블 삭제

DROP TABLE syntax

DROP TABLE table_name;
- DROP TABLE statement 이후 삭제할 테이블 이름 작성

타입 선호도(Type Affinity)
- 컬럼에 데이터 타입이 명시적으로 지정되지 않았거나 지원하지 않을 때 SQLite가 자동으로 데이터 타입을 추론하는 것

타입 선호도 목적

1. 유연한 데이터 타입 지원
- 데이터 타입을 명시적으로 지정하지 않고도 데이터를 저장하고 조회할 수 있음
- 컬럼에 저장되는 값의 특성을 기반으로 데이터 타입을 유추

2. 간편한 데이터 처리
- INTEGER Type Affinity를 가진 열에 문자열 데이터를 저장해도 SQLite는 자동으로 숫자로 변환하여 처리
  
3. SQL 호환성
- 다른 데이터베이스 시스템과 호환성을 유지

반드시 NOT NULL 제약을 사용할 필요는 X

하지만 데이터베이스를 사용하는 프로그램에 따라 NULL을 저장할 필요가 없는 경우가 많으므로 대부분 NOT NULL을 정의

"값이 없다."라는 표현을 테이블에 기록하는 것은 '0'이나 '빈 문자열'등을 사용하는 것으로 대체하는 것을 권장

INSERT statement : 테이블 레코드 삽입

INSERT INTO table_name (c1, c2, ...)
VALUES (v1,v2, ...);

UPDATE statement : 테이블 레코드 수정

UPDATE syntax

UPDATE table_name
SET column_name = expression,
[WHERE
  condition];

- SET 절 다음에 수정할 필드와 새 값을 지정
- WHERE 절에서 수정할 레코드를 지정하는 조건 작성
- WHERE 절을 작성하지 않으면 모든 레코드를 수정

DELETE statement : 테이블 레코드 삭제

DELETE FROM table_name
[WHERE
  condition];

- SQLite에는 날짜 및/또는 시간을 저장하기 위한 별도 데이터 타입이 없음
- 대신 날짜 및 시간에 대한 함수를 사용해 표기 형식에 따라 TEXT, REAL, INTEGER 값으로 저장

JOIN이 필요한 순간
- 테이블을 분리하면 데이터 관리는 용이해질 수 있으나 출력시에는 문제가 있음
- 테이블 한 개 만을 출력할 수 밖에 없어 다른 테이블과 결합하여 출력하는 것이 필요해짐

JOIN clause : 둘 이상의 테이블에서 데이터를 검색하는 방법

JOIN 종류 : INNER JOIN, LEFT JOIN

INNER JOIN clause : 두 테이블에서 값이 일치하는 레코드에 대해서만 결과를 반환

INNER JOIN syntax

SELECT
  select_list
FROM
  table_a
INNER JOIN table_b
  ON table_b.fk = table_a.pk

- FROM절 이후 메인 테이블 지정 (table_a)
- INNER JOIN 절 이후 메인 테이블과 조인할 테이블을 지정 (table_b)
- ON 키워드 이후 조인 조건을 작성
- 조인 조건은 table_a과 table_b 간의 레코드를 일치시키는 규칙을 지정

LEFT JOIN clause : 오른쪽 테이블의 일치하는 레코드와 함께 왼쪽 테이블의 모든 레코드 반환

LEFT JOIN syntax

SELECT
  select_list
FROM
  table_a
LEFT JOIN table_b
  ON table_b.fk = table_a.pk

- FROM절 이후 왼쪽 테이블 지정 (table_a)
- LEFT JOIN 절 이후 오른쪽 테이블 지정 (table_b)
- ON 키워드 이후 조인 조건을 작성
- 왼쪽 테이블의 각 레코드를 오른쪽 테이블의 모든 레코드와 일치시킴

LEFT JOIN 특징
- 왼쪽은 테이블의 모든 레코드를 표기
- 오른쪽 테이블과 매칭되는 레코드가 없으면 NULL을 표시

Many to one relationships(N:1 or 1:N)
- 한 테이블의 0개 이상의 레코드가 다른 테이블의 레코드 한 개와 관련된 관계

Comment-Article : 0개 이상의 댓글은 1개의 게시 글에 작성 될 수 있다.

ForeignKey() - N:1 관계 설정 모델 필드

ForeignKey() 클래스의 인스턴스 이름은 참조하는 모델 클래스 이름의 단수형으로 작성하는 것을 권장

ForeignKey 클래스를 작성하는 위치와 관계 없이 외래 키는 테이블 필드 마지막에 생성됨 

ForeignKey(to, on_delete)
- to : 참조하는 모델 class 이름
- on_delete : 외래 키가 참조하는 객체(1)가 사라졌을 때, 외래 키를 가진 객체(N)를 어떻게 처리할 지를 정의하는 설정(데이터 무결성)

on_delete의 'CASCADE'
- 부모 객체(참조 된 객체)가 삭제 됐을 때 이를 참조하는 객체도 삭제

Migration
- 댓글 테이블의 article_id 필드 확인
- 참조하는 클래스 이름의 소문자(단수형)로 작성하는 것이 권장 되었던 이유 : '참조 대상 클래스 이름' + '_' + '클래스 이름'

역참조 
- N:1 관계에서 1에서 N을 참조하거나 조회하는 것 1 -> N
- N은 외래 키를 가지고 있어 물리적으로 참조가 가능하지만 1은 N에 대한 참조 방법이 존재하지 않아 별도의 역참조 이름이 필요

역참조 사용 예시 
- 모델 인스턴스.related manager(역참조 이름).QuerySet API

related manager
- N:1 혹은 M:N 관계에서 역참조 시에 사용하는 매니저
- 'objects' 매니저를 통해 queryset api를 사용했던 것처럼 related manager를 통해 queryset api를 사용할 수 있게 됨

related manager 이름 규칙
- N:1 관계에서 생성되는 Related manager 이름은 참조하는 "모델명_set" 이름 규칙으로 만들어짐
- 해당 댓글의 게시글(Comment -> Article) : comment.article
- 게시글의 댓글 목록(Article -> Comment) : article.comment_set.all

댓글 CREATE 구현
- 사용자로부터 댓글 데이터를 입력 받기 위한 CommentForm 정의
- detail view 함수에서 CommentForm을 사용하여 detail 페이지에 렌더링
- Comment 클래스의 외래 키 필드 article 또한 데이터 입력이 필요한 필드이기 때문에 출력 되고 있는 것
- 하지만, 외래 키 필드는 사용자 입력 값으로 받는 것이 아닌 view 함수 내에서 다른 방법으로 전달 받아 저장되어야 함
- CommentForm의 출력 필드 조정
- url 작성 및 action 값 작성
- comments_create view 함수 정의

save(commit=False) : DB에 저장하지 않고 인스턴스만 반환

- save의 commit 인자를 활용해 외래 키 데이터 추가 입력
- 댓글 작성 후 테이블 확인

댓글 READ 구현
- detail view 함수에서 전체 댓글 데이터를 조회
- 전체 댓글 출력 및 확인


댓글 DELETE 구현
- 댓글 삭제 url 작성
- 댓글 삭제 view 함수 정의
- 댓글 삭제 버튼 작성
- 댓글 삭제 버튼 출력 확인 및 삭제 테스트

admin site 등록 : Comment 모델을 admin site에 등록해 CRUD 동작 확인하기

댓글이 없는 경우 대체 콘텐츠 출력 : DTL 'for empty' 태그 사용

댓글 개수 출력하기
- DTL filter : 'length' 사용
- Queryset API : 'count()' 사용

User 모델을 참조하는 2가지 방법
- get_user_model(), settings.AUTH_USER_MODEL

get_user_model()
- 반환 값 : User Object(객체), 사용 위치 : models.py가 아닌 다른 모든 위치

settings.AUTH_USER_MODEL 
- 반환 값 : accounts.User(문자열), 사용 위치 : models.py

Migration
- 기본적으로 모든 컬럼은 NOT NULL 제약 조건이 있기 때문에 데이터가 없이는 새로운 필드가 추가되지 못함 : 기본값 설정 필요
- 1을 입력하고 Enter 진행
- 추가되는 외래 키 user_id에 어떤 데이터를 넣을 것인지 직접 입력해야 함
- 마찬가지로 1 입력하고 Enter 진행
- 그러면 기존에 작성된 게시글이 있다면 모두 1번 회원이 작성한 것으로 처리됨
- migrations 파일 생성 후 migrate 진행
- article 테이블의 user_id 필드 생성 확인

게시글 CREATE
- 기존 ArticleForm 출력 변화 확인
- User 모델에 대한 외래 키 데이터 입력을 위해 불필요한 input이 출력
- ArticleForm 출력 필드 수정
- 게시글 작성 시 에러 발생
- user_id 필드 데이터가 누락되었기 때문
- 게시글 작성 시 작성자 정보가 함께 저장될 수 있도록 save의 commit 옵션 활용
- 게시글 작성 후 테이블 확인

게시글 READ
- 각 게시글의 작성자 이름 출력

게시글 UPDATE
- 게시글 수정 요청 사용자와 게시글 작성 사용자를 비교하여 본인의 게시글만 수정 할 수 있도록 하기
- 해당 게시글의 작성자가 아니라면, 수정/삭제 버튼을 출력하지 않도록 하기

게시글 DELETE
- 삭제를 요청하려는 사람과 게시글을 작성한 사람을 비교하여 본인의 게시글만 삭제 할 수 있도록 하기

Comment - User 모델 관계 설정 : User 외래 키 정의

Migration 
- 이전에 Article와 User 모델 관계 설정 때와 동일한 상황
- 기존 Comment 테이블에 새로운 컬럼이 빈 값으로 추가 될 수 없기 때문에 기본 값 설정 과정이 필요
- comment 테이블 user_id 필드 확인

댓글 CREATE
- 댓글 작성 시 이전에 게시글 작성할 때와 동일한 에러 발생
- 댓글의 user_id 필드 데이터가 누락되었기 때문
- 댓글 작성 시 작성자 정보가 함께 저장할 수 있도록 작성
- 댓글 작성 후 테이블 확인

댓글 READ
- 댓글 출력 시 댓글 작성자와 함께 출력

댓글 DELETE
- 댓글 삭제 요청 사용자와 댓글 작성 사용자를 비교하여 본인의 댓글만 삭제 할 수 있도록 하기
- 해당 댓글의 작성자가 아니라면, 댓글 삭제 버튼을 출력하지 않도록 함

@login_required : 인증된 사용자만 댓글 작성 및 삭제

Many to many relationships(N:M or M:N)
- 한 테이블의 0개 이상의 레코드가 다른 테이블의 0개 이상의 레코드와 관련된 경우(양쪽 모두에서 N:1 관계를 가짐)

Django에서는 'ManyToManyField'로 중개모델을 자동으로 생성

'through' argument : 중개 테이블에 '추가 데이터'를 사용해 M:N 관계를 형성하려는 경우에 사용

M:N 관계 주요 사항
- M:N 관계로 맺어진 두 테이블에는 물리적인 변화가 없음
- ManyToManyField는 중개 테이블을 자동으로 생성
- ManyToManyField는 M:N 관계를 맺는 두 모델 어디에 위치해도 상관 없음
  (대신 필드 작성 위치에 따라 참조와 역참조 방향을 주의할 것)
- N:1은 완전한 종속의 관계였지만 M:N은 종속적인 관계가 아니며 '의사에게 진찰받는 환자 & 환자를 진찰하는 의사' 이렇게 2가지 형태 모두 표현 가능

ManyToManyField(to, **options) : Many to many 관계 설정 시 사용하는 모델 필드

ManyToManyField's Argument

1. 'related_name' arguments 
- 역참조시 사용하는 manager name을 변경

2. 'symmetrical' arguments 
- ManyToManyField가 동일한 모델을 가리키는 정의에서만 사용
- 기본 값 : True

True일 경우
- source 모델의 인스턴스가 target 모델의 인스턴스를 참조하면 자동으로 target 모델 인스턴스도 source 모델 인스턴스를 자동으로 참조하도록 함(대칭)
- 즉, 자동으로 내가 당신의 친구라면 당신도 내 친구가 됨

False일 경우
- True였을 때와 반대(대칭되지 않음)

M:N에서의 methods

1. add()
- "지정된 객체를 관련 객체 집합에 추가"(이미 존재하는 관계에 사용하면 관계가 복제되지 않음)
  
2. remove() 
- "관련 객체 집합에서 지정된 모델 객체를 제거"

Article(M) - User(N) : 0개 이상의 게시글은 0명 이상의 회원과 관련
- 게시글은 회원으로부터 0개 이상의 좋아요를 받을 수 있고, 회원은 0개 이상의 게시글에 좋아요를 누를 수 있음

User - Article간 사용 가능한 전체 related manager

1. article.user - 게시글을 작성한 유저 - N:1
2. user.article_set - 유저가 작성한 게시글(역참조) - N:1
3. article.like_users - 게시글을 좋아요 한 유저 - M:N
4. user.like_articles - 유저가 좋아요 한 게시글(역참조) - M:N

User(M) - User(N) : 0명 이상의 회원은 0명 이상의 회원과 관련
- 회원은 0명 이상의 팔로워를 가질 수 있고, 0명 이상의 다른 회원들을 팔로잉 할 수 있음

참조 - 내가 팔로우하는 사람들(팔로잉, followings)
역참조 - 상대방 입장에서 나는 팔로워 중 한 명(팔로워, followers)

.exists() : QuerySet에 결과가 포함되어 있으면 True를 반환하고 결과가 포함되어 있지 않으면 False를 반환
- 큰 QuerySet에 있는 특정 객체 검색에 유용

Fixtures : Django가 데이터베이스로 가져오는 방법을 알고 있는 데이터 모음
- 데이터베이스 구조에 맞추어 작성 되어있음

fixtures 관련 명령어
dumpdata : 생성(데이터 추출), loaddata : 로드(데이터 입력)

dumpdata : 데이터베이스의 모든 데이터를 추출
- 추출한 데이터는 json 형식으로 저장

loaddata : Fixtures 데이터를 데이터베이스로 불러오기

Fixtures 파일 기본 경로 : app_name/fixtures/
- Django는 설치된 모든 app의 디렉토리에서 fixtures 폴더 이후의 경로로 fixtures 파일을 찾아 load

loaddata 순서 주의사항

만약 loaddata를 한 번에 실행하지 않고 하나씩 실행한다면 모델 관계에 따라 load하는 순서가 중요할 수 있음
- comment는 article에 대한 key 및 user에 대한 key가 필요
- article은 user에 대한 key가 필요

즉, 현재 모델 관계에서는 user -> article -> comment 순으로 data를 넣어야 오류가 발생하지 않음

loaddata시 encoding codec 관련 에러가 발생하는 경우

1. dumpdata시 추가 옵션 작성
- python -Xutf8 manage.py dumpdata

2. 메모장 활용
- 메모장으로 json 파일 열기
- "다른 이름으로 저장" 클릭
- 인코딩을 UTF8로 선택 후 저장

Fixtures 파일을 직접 만들지 말 것 : 반드시 dumpdata 명령어를 사용하여 생성

Improve query : 같은 결과를 얻기 위해 DB 측에 보내는 쿼리 개수를 점차 줄여 조회하기

annotate : SQL의 GROUP BY 쿼리를 사용

select_related : SQL의 INNER JOIN 쿼리를 활용
- 1:1 또는 N:1 참조 관계에서 사용

