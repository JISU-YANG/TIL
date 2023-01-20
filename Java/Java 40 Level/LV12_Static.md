## JAVA 40 LEVEL
# Lv.12 Static

### Static의 메모리 영역

메모리는 크게 3가지로 분류할 수 있다.
1. Method Area(스태틱, 메서드)
2. Stack(변수 명, 타입, 값, 연산)
3. Heap(인스턴스, 생성자)

---

### Static의 이점

1. 항상 값이 변하지 않는 경우라면 메모리 할당을 한번만 하게 되어 메모리 사용의 이점이 있다.
2. 같은 메모리 주소를 바라보게 되어 변수를 공유하여 값을 컨트롤 할 수 있다.

---

### Static의 접근

- static은 static을 접근할 수 있다.
- static은 non-static을 접근할 수 없다.
- non-static은 static을 접근할 수 있다.
- non-static은 non-static을 접근할 수 있다.