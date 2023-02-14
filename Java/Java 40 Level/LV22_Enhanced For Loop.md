## JAVA 40 LEVEL
# Lv.21 String 2, Parsing

> 향상된 for문이라고도 한다.

### 용도
배열을 다루는 로직일때 사용된다.

### 장점
- Index와 객체 호출을 사용하지 않는다.
- 객체 배열의 처음부터 끝까지 출력하므로 index exception가 절대 발생하지 않는다.
- 자동으로 타입 캐스팅 할 수 있다.


### 단점
- 중간에 멈출 수 없다.
- index를 알 수 없다.
- 값을 수정할 수 없다.


### 예시
```Java
class Ex(){
    int [] a = {1,2,3};

    {
        for (int b : a) { // javascript에서는 (int b in a)
            System.out.print(b);
        }
    }
}

```