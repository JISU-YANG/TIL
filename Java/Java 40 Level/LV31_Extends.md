JAVA 40 LEVEL
# Lv.31 Extends

### Extends, Implements
부모 Class의 특성을 Member로 확장시킨다.

### Extends
같은 부모를 중복으로 상속받는 형태가 되기때문에 다중 상속은 되지 않고 단일 상속만 가능하다.

### Java의 Class 종류
1. Class: extends
2. Enum(절차식)
3. Interface: implements

### 특징
- Interface끼리 Extends하면 합치는 형태가 된다.

</br>

![Extends Image](/Source/Extends.png)

</br>

- 하위 클래스는 상위 클래스와 오브젝트 클래스에 접근이 가능하다.

</br>

```java
public class ex(){
    public static void main(String[] args){
        Child c1 = new Child();
        Child_Two c2 = new Child_Two();
        c1.parentsPrint();
        c2.parentsPrint();
        c2.child_Two_Print();

        // 코드에는 문제가 없지만 클래스의 기능을 잃어버리기 때문에
        // ClassCastException이 발생한다.
        Object o1 = c1;
        Object o2 = c2;

        Child_Two cc1 = (Child_Two)o1;
        Child cc2 = (Child)o2;
    }
}
```
