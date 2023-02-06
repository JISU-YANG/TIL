## JAVA 40 LEVEL
# Lv.17 Short Circuit

### 숏 서킷
&(엔퍼센트)와 |(브로큰바)를 이용해 논리연산이 이루어질때 앞의 결과에 따라 뒤의 연산을 생략할 수 있다.

### &&(AND, 논리곱)
a && b: a와 b 모두 true일 경우 true

### ||(OR, 논리합)
a || b: a와 b 중 하나만 true이어도 true

### Tip
가장 false가 많이 나오는 연산부터 작성하면 연산이 단축되는 효과가 있다.
더 줄일려면 객체지향, 디자인 패턴 순으로 적용해본다.

```java
package jisu.log;

public class ShortCirCuit {
    public void check() {
        if(isTrue() && isFalse()); // True, False 출력
        if(isTrue() && isTrue()); // True, True 출력
        if(isFalse() && isTrue()); // False만 출력
        if(isFalse() && isFalse()); // False만 출력
    }
    
    public boolean isTrue() {
        boolean isc = true;
        System.out.println(isc);
        return isc;
    }

    public boolean isFalse() {
        boolean isc = false;
        System.out.println(isc);
        return isc;
    }
}

```