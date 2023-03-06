2019.08.11
# Oracle DB의 Type과 Concatenation

> 벤더사마다 차이는 있지만 ORACLE기준으로 타입은 3가지이다.

## 자주 쓰는 데이터 유형

### 문자
- CHAR(index)
- VARCHAR2(index)
    - VARCHAR는 최대 4000자, VARCHAR2는 최대 8000자까지 지원된다 

### 숫자
- NUMBER (index, 부동소수점)
    - 지정한 부동소수점은 총 index에서 제한다.  

### 날짜 
- DATE
    - 년월일시분초
- TIMESTAMP
    - DATE+밀리초

---

## CONCATENATION
### DB에서 문자열 합치기 
- || (Oracle) 
- \+ (SQL Server)
- CONCAT(String1, String2) 

### 날짜형 데이터의 연산 
- 날짜형 데이터 + 숫자형 데이터(기본 단위 1일)
- 날짜형 데이터 + 문자형 데이터(숫자형 데이터로 변환이 가능한)
