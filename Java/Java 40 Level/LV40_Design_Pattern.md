JAVA 40 LEVEL
# Lv.40 Design Pattern

1. ProtoType Pattern
   - 프로토 타입 패턴이란 인스턴스를 새로 생성하는 것이라 생성된 인스턴스로부터 별도의 인스턴스를 만드는 것
   - 클래스의 인스턴스를 생성한다.
   - 생성된 인스턴스를 복제한다. (값은 유지하지만 객체를 변경한다.)
      - 인스턴스를 만들고 값을 복사하고 다시 넣으면 속도가 느려서
      - Framework와 Instance를 분리하기 위해
      - Instance의 값은 변화시키지 않고 사용할 때
   - ```java
     public class A implements Cloneable{
        @Override
        protected Obejct clone(){
            return super.clone(); // 사용할 때 CloneNotSupportedException 발생 복제 클래스를 허용하지 않는 예외
        }
     }
     ```
2. SingleTon Pattern
    - 특정 클래스의 인스턴스를 한번만 생성하도록 한다.
    - Heap 영역에 단 하나의 인스턴스를 생성되도록 한다.
    - 생성방법
      1. 생성자를 Private으로 선언한다.
      2. 객체를 판별하고 객체의 주소를 담을 수 있는 공간을 Member Field에 선언한다.
      3. Member Field의 공간에 null, 인스턴스 여부를 판단하여 클래스 안에서 인스턴스를 생성한다.
3. Iterator Pattern
   - Iterator은 컬렉션 프레임워크, StringTokenizer 클래스에서 implements해서 구현해놓은 클래스이다.(java.util.Iterator)
   - 메소드
      - 확인하는 메소드 hasNext()
      - 출력하는 메소드 next()
      - 삭제하는 메소드 remove()
4. Factory Pattern
   - 상속 구조가 되어있는 클래스는 골격(추상 클래스, 인터페이스)만을 가지고 있다.
   - 실질적으로 인스턴스는 하위 클래스에서 작성된 것이 사용된다.
   - 골격으로 자식의 클래스의 메소드를 invoke한다.
   - 구조를 단순화 시킬 수 있고, 코드 재사용성을 높일 수 있다.
5. Templete Method Pettern
   - Abstract, Interface를 이야기한다.
   - 하나 이상의 알고리즘(로직풀이) 과정에서 하위 클래스에서 재구현(Override)해 사용한다.
   - 알고리즘을 구현하기 위한 골격은 유지한 채 다른 동작을 실행할 수 있도록 한다.