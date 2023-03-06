2019.08.11
# Oracle DB의 Tablespace

### TABLESPACE
- 물리적인 공간
- 계정, TABLE(ENTITY)만 생성하고 SCHEMA는 건들지 않는다.
- DBA_DATA_FILES에 있다.


### SCHEMA
DB의 자료, 표현, 관계구조를 나타내는 껍대기

### TEMPORARY TABLESPACE
연산, SORT 작업 등에 사용되기 위해 존재한다.

### TABLESPACE QUERY
1. 위치확인
    ```sql
    SELECT FILE_NAME, TABLESPACE_NAME, AUTOEXTENSIBLE FROM DBA_DATA_FILES;
    ```
2. 테이블스페이스 생성
    ```sql
    CREATE TABLESPACE 테이블스페이스이름 DATAFILE ‘경로/파일이름.dbf' SIZE 200M AUTOEXTEND ON NEXT 5M MAXSIZE 300M;
    ```
3. 계정에 기본 테이블 스페이스 지정
    ```sql
    ALTER USER 계정 DEFAULT TABLESPACE 테이블스페이스명;
    ```
4. 임시 테이블 스페이스 선언
    ```sql
    ALTER USER 계정 TEMPORARY TABLESPACE 임시테이블스페이스명;
    ```
5. DBA, RESOURCE, CONNECT 권한부여
    ```sql
    GRANT DBA, RESOURCE, CONNECT TO 계정명;
    ```
6. DBA, RESOURCE, CONNECT 권한해제
    ```sql
    REVOKE DBA, RESOURCE, CONNECT FROM 계정명;
    ```