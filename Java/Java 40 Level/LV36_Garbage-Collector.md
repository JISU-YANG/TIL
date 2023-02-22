JAVA 40 LEVEL
# Lv.36 Garbage Collector

1. 메모리의 Heap 영역에 객체가 생성된다.
2. 사용하지 않는 객체는 가비지 컬렉터의 삭제 대상이 된다.

### 가비지 컬렉터의 역할
삭제 대상 객체가 Stack에 묶여있지 않은지 확인하고 JVM이 가비지 컬렉터를 작동시켜 메모리에서 제거한다.


### 가비지 컬렉터의 특이사항
- java.lang.System.gc()를 통해서 가비지 컬렉터를 실행시킬 수 있지만, JVM을 거쳐 제거될 수도 있고 안 될 수도 있다.
- java.lang.finalize() 메소드는 객체가 삭제되면 호출된다. // Java 9~, java.lang.ref.Cleaner()