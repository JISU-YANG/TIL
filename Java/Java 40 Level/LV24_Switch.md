## JAVA 40 LEVEL
# Lv.24 Switch

> Switch문은 선택 조건문이라고 부른다.

### fall-throw 기법
- 값이 일치하는 case부터 break를 만날때까지 지속적으로 코드가 실행된다.
- 값에 해당하는 case가 없으면 default가 실행된다.

### 특징
- key와 case value의 타입이 같아야 하고 값이 필요하다.
- JDK 1.6 에서 사용할 때 반드시 정수만을 사용한다.
- JDK 1.7 부터는 String 타입을 지원한다.
- 1:1 매핑이기 때문에 if문(범위 조건문)과 대체가 불가능하다.