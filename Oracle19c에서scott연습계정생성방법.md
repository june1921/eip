Oracle19c에서 scott 계정을 생성하다보면 다음과 같은 오류를 만날수 있다.
```
CREATE USER SCOTT IDENTIFIED BY TIGER  
오류 보고 -  
ORA-65096: 공통 사용자 또는 롤 이름이 부적합합니다.  
65096. 00000 -  "invalid common user or role name"  
```
그때는 유저이름에 c##을 붙여주면 된다.  
c##을 안붙이고 싶다면  
```
alter session set "_ORACLE_SCRIPT"=true;
```
와 같이 쓰면 된다.