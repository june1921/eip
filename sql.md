# 8장 SQL 응용
## 118. SQL - DDL
### 1. DDL(Data Define Language, 데이터 정의어)
CREATE, ALTER, DROP. DB를 쓰면서 얼마나 쓸일이 있냐만은 일단은 정리 차원에서 적어둔다.
* CREATE: SCHEMA, DOMAIN, TABLE, VIEW, INDEX를 정의함   
* ALTER: TABLE에 대한 정의를 변경하는 데 사용함  
* DROP: SCHEMA, DOMAIN, TABLE, VIEW, INDEX를 삭제함
### 2. CREATE SCHEMA
```
CREATE SCHEMA 스키마명 AUTHORIZATION 사용자_id;  
```
소유권자의 사용자 ID가 '홍길동'인 스키마 '대학교'를 정의하는 SQL문  
```
CREATE SCHEMA 대학교 AUTHORIZATION 홍길동;
```
### 3. CREATE DOMAIN
```
CREATE DOMAIN 도메인명[AS] 데이터_타입
    [DEFAULT 기본값]
    [CONSTRAINT 제약조건명 CHECK (범위값)];
```
여기서 대괄호 []로 표시된 것은 생략 가능하다는 뜻이다.
* 데이터 타입: SQL에서 지원하는 데이터 타입
* 기본값: 데이터를 입력하지 않았을 때 자동으로 입력되는 값   

'성별'을 '남' 또는 '여'와 같이 정해진 1개의 문자로 표현되는 도메인 SEX를 정의하는 SQL문은 다음과 같다.
```
CREATE DOMAIN SEX CHAR(1)
    DEFAULT '남'
    CONSTRAINT VALID-SEX CHECK(VALUE IN('남', 여));
```
### 4. CREATE TABLE
