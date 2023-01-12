## JAVA 40 LEVEL
# Lv.10 Auto Boxing

각 기본 타입에는 래퍼 클래스(Wrapper Class)가 존재한다.

ex) int와 Integer, char와 Character

>Auto Boxing(기본 타입을 참조 타입으로 변환)과 Auto Unboxing(참조타입을 기본타입으로 변환)은 JDK 1.5부터 자동으로 작동되기 시작했다.

```java
int a1 = 10;

// Outo Boxing
Integer a2 = a1; // 기본 타입 -> 참조 타입 자동 변환

// Outo Unboxing
int a3 = a2; // 참조 타입 -> 기본 타입 자동 변환

// Old Style
int a4 = a2.intValue()
 
```

메모리에서 Stack과 Heap 영역에서 값이 이동된다.