### Java

# static 예약어를 import에 사용하기


</br>

## static import의 장단점

### 장점
- import되는 Library를 바로 Member처럼 접근할 수 있다.
- 코드를 짧게 쓸 수 있고, 가독성을 높일 수 있다.

### 단점
- 잘못 사용하면 가독성을 오히려 해칠 수 있다.
- 네임스페이스가 오염될 수 있다. (명명이 겹치는 경우)

</br>

## 코드 예시
### 일반적인 import 사용시
```java
import java.lang.Math.*;

...

double a = Math.abs(123.456) * Math.PI;

```
### static을 이용한 import 사용시
```java
// import static java.lang.Math.*;
import static java.lang.Math.abs;
import static java.lang.Math.PI;

...

double a = abs(123.456) * PI;

```
추가로 import static을 사용할 때는 [와일드 카드를 권장하지 않는다.](https://docs.oracle.com/javase/1.5.0/docs/guide/language/static-import.html)
