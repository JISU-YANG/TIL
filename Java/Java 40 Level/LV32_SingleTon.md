JAVA 40 LEVEL
# Lv.32 Single Ton Pattern

> ### 목적
>
> 메모리에 객체를 한번만 생성하여 같은 객체로 사용한다.

```java
public class SingleTon {
    /*
     * 3. 선언
     * 객체의 주소를 담을 수 있는 변수를 선언한다.
     */
    private static SingleTon instance;

    /*
     * 1. 생성자 제한
     * 외부에서 객체를 접근할 수 없도록 생성자를 제한한다.
     */
    private SingleTon(){}

    /*
     * 2. 인스턴스 존재 확인
     * 외부에서 객체의 주소를 판단하여 Heap에 주소를 가지고 있다면 주소를 반환해주고
     * 만약, 주소가 없다면(Null) 자신이 생성자를 instance화 하여 그 주소를 반환해준다.
     * 클래스에 접근할 수 없기 때문에 static을 사용하여 생성 
     */
    public static SingleTon getInstance() {
        // 객체의 존재 유무를 판단하려면 null or reference
        if (instance == null) {
            instance = new SingleTon();
        }
        return instance;
    }
}
```


 

### 추가 디자인 패턴
- Factory: polymorphism
- Template: clone()
- Delegate: Bean(ioc)