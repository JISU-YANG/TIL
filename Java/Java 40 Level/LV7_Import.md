## JAVA 40 LEVEL
# Lv.7 Import

### 임폴트(Import)
Class의 최상단부에 사용된 API의 위치를 명시적으로 표시해준다.

---

### 임폴트(Import)의 예시
- 기본 자료형에 관련된 것들은 java.lang 패키지 하위에 속한다.
  - ex) java.lang.integer
- 기본 유틸들은 java.util 패키지 하위에 속한다.
  - ex) java.lang.random

---

### 임폴트(Import)의 예외
기본적으로 선언부에 패키지 위치를 명시적으로 표시하지만, 예외적으로 암묵적으로 표시하지 않는 경우도 있다.

- 같은 패키지면 표시되지 않는다.
- 사용빈도가 아주 높은 Class들은 표시되지 않는다.
  - ex) java.lang.String