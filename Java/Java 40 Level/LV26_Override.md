## JAVA 40 LEVEL
# Lv.26 Override

> 메소드 오버라이딩, 재정의라고도 부른다.

### 조건
오직 super(부모)와 sub(자식)의 관계에서만 발생된다.

### 의미
부모의 메소드 코드 블록안의 프로세스를 다시 정의한다.

### 예외
- private은 extends되지 않기 때문에 대상이 아니다.
- 부모의 메소드는 final일 경우 대상이 아니다.
- 부모의 생성자는 대상이 아니다.