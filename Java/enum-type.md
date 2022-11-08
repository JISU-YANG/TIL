### Java
# Enum Type
JDK 1.5부터 C/C++(int Value) 보다 향상된 성능의 Enum 클래스를 지원한다.

</br>

## Enum Type을 왜 사용할까?
### 관련있는 상수들을 개별로 선언하지 않고 몇 가지 문제점을 보완해준다.
- 개발자의 실수를 차단해준다.
- 한 눈에 알아보기 쉽다. 접두어가 필요 없어 변수명을 깔끔하게 사용할 수 있다.
- 편리한 기능을 사용할 수 있다. 로직을 추가하는 것도 가능하다.
- 식별자 하나만 더 추가하면 되기 때문에 유지보수가 쉬워진다.
- 싱글톤으로 생성되기 때문에 어디서나 접근이 가능하다.

</br>

## Enum Type은 어떻게 사용할까?
### 기본적인 형태의 Enum 클래스 정의
```java
public enum Day{
    MOM, TUE, WED, THU, FRI, SAT, SUN
}
```
---
### 필드가 추가된 Enum 클래스 정의
```java
public enum Day {
    MON("Monday","Mon",0),
    TUE("Tuesday","Tue",1),
    WED("Wednesday","Wed",2),
    THU("Thursday","Thu",3),
    FRI("Friday","Fri",4),
    SAT("Saturday","Sat",5),
    SUN("Sunday","Sun",6);

    private String full;
    private String lower;
    private int index;

    Day(String full, String lower, int index) {
        this.upper = full;
        this.lower = lower;
        this.index = index
    }

    // @Getter
    public String getFull() {
        return full;
    }

    public int getLower() {
        return lower;
    }

    public int getIndex() {
        return index;
    }
}
```
여기에 추가로 index로 upper 가져오기와 같은 사용하고자 하는 로직을 추가할 수도 있다. Lombok 어노테이션을 사용한다면 더 쉽고 깔끔하게 사용할 수 있다. index의 경우는 사실 정의하지 않아도 ordinal()로 얻을 수 있다.

```java
class Main{
    public static void main(String[] args){
        System.out.println(Day.SUN); // SUN
        System.out.println(Day.SUN.getFull()); // Sunday
    }
}
```

</br>

## Enum Type의 기능을 알아보자
### 대표적인 Enum 메소드
- static E values()
해당 Enum의 모든 상수를 배열로 반환한다.

- static E valueOf(String name)
전달된 문자열과 일치하는 필드의 상수를 반환한다.

- protected void finalize()
해당 Enum 클래스가 final 메소드를 가질 수 없게 된다.

- String name()
해당 상수의 이름을 반환한다.

- int ordinal()
해당 상수가 정의된 순서에 따라 index를 반환한다.

---

### 개발자가 정의한 필드를 컨트롤하는 메소드
직접 순회, 캐싱으로 순회 피하기 등
[필드 값으로 Enum 값 찾기](https://bcp0109.tistory.com/334)

---

### Enum 활용하기
[우아한형제들 기술블로그 Java Enum 활용기](https://techblog.woowahan.com/2527/)

</br>

## 레퍼런스
- [Enum 하나가 if문 여러개보다 낫다](https://velog.io/@skyepodium/enum-하나가-if-문-여러개-보다-낫다)
