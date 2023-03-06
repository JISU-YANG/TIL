2019.08.11
# 관계형 데이터 베이스 관리 시스템

### RDBMS란
- 관계형 데이터베이스 매니지먼트 시스템
- 정규화 공식에 의해 테이블간 관계를 가지고 있는게 특징이다.
- SQL을 사용한다.
- DB 시스템의 정규화를 통해 이상현상을 제거하고 무결성을 보장한다.

### 구조
- DCL(+TCL) : 권한 및 Transaction 제어
  - ex) DCL : GRANT, REVOKE, TCL : COMMIT, ROLLBACK

- DDL : 데이터 구조 정의
  - ex) ALTER, DROP, CREATE, RENAME

- DML : 데이터 관리
  - ex) SELECT, UPDATE, DELETE, INSERT

### ACID
ACID하기 때문에 Transaction의 안전성을 보장할 수 있다.
</br>
(All or Nothing 전략)
 
- Atomic 원자성 
- Consistency 일관성
- Isolation 독립성
- Durabiliry 지속성
