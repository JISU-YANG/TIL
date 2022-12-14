### 클래스 리터럴이란
---
```java
public class ClassLiterals{
    public static void main(String[] args){
        System.out.println(Object.class);
    }
}
```

위 코드에서 ".class" 부분이 Java SE의 클래스 리터럴(Class Literals)이다.



## 클래스 리터럴의 사용
---
1. 클래스(class)
2. 인터페이스(interface)
3. 배열 타입(array type)
4. 기본 타입(primitive type)
5. void(the pseudo-type void)

뒤에 "."과 함께 "class" 토큰으로 붙여 표현할 수 있다.


## 클래스 리터럴의 정리
---
".class"를 가능하게 하는 Class 클래스를 보면 이렇다.

```java
public final class Class<T> extends Object implements Serializable, GenericDeclaration, Type, AnnotatedElement
```

Class 클래스는 public 생성자가 없으며 JVM에 의해 자동적으로 생성된다. 이 인스턴스는 레퍼런스(Reference)를 지닌다.


__즉, Ex.class에 의한 리턴 값은 Class<Ex>의 참조 값이다.__

\+

또한, getClass 메소드를 통해서도 같은 값을 얻을 수 있다.