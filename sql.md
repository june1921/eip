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
```
CREATE TABLE 테이블명
    (속성명 데이터_타입 [DEFAULT 기본값] [NOT NULL], ...
    [, PRIMARY KEY(기본키_속성명, ...)]
    [, UNIQUE(대체키_속성명, ...)]
    [, FOREIGN KEY(외래키_속성명, ...)
        REFERENCES 참조테이블(기본키_속성명, ...)]
        [ON DELETE 옵션]
        [ON UPDATE 옵션]
    [, CONSTRAINT 제약조건명][CHECK (조건식)]);
```
* 기본 테이블에 포함될 모든 속성에 대하여 속성명과 그 속성의 데이터 타입, 기본값, NOT NULL 여부를 지정한다.
* PRIMARY KEY: 기본키로 사용할 속성을 지정함
* UNIQUE: 대체키로 사용할 속성을 지정함, 중복된 값을 가질 수 없음
* FOREIGN KEY ~ REFERENCES ~: 외래키로 사용할 속성을 지정함
  - ON DELETE 옵션: 참조 테이블의 튜플이 삭제되었을 때 기본 테이블에 취해야 할 사항을 지정함
  - ON UPDATE 옵션: 참조 테이블의 참조 속성 값이 변경되었을 때 기본 테이블에 취해야 할 사항을 지정함