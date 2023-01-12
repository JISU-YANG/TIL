## JAVA 40 LEVEL
# Lv.8 Primitive Type

### 기본형 타입 (Primitive Type)
- 문자, 숫자, 논리(T/F)와 같은 값(Value)을 담기 위한 공간의 종류를 말한다.
  - 프로그래밍에서는 효율을 굉장히 중시하며 각각 타입에 따라 메모리에 할당되는 크기, 값의 범위까지 달라진다.

---

### 기본형 타입 (Primitive Type)의 특징
- 메모리(Memory)의 스택(Stack)영역에 위치한다.
- 변수는 값을 참조하고 있다. (pass by value)
- Mutable(대상이 변하는)한 성질을 지니고 있다.
- 정수형, 실수형 변수의 가장 앞 비트는 부호비트를 가지고 있다.

---

### 기본형 타입 (Primitive Type)의 종류
|분류|정수형|||||실수형(부동소수점)|논리형|문자형|
|---|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
|기본값|0|||||0.0|false|\u0000|
|타입|byte|short|int|long|float|double|boolean|char|
|크기|1byte (8bit)|2byte (16bit)|4byte (32bit)|8byte (64bit)|4byte (32bit)|8byte (64bit)|1byte (8bit)|2byte (16bit)|
|값|-128 ~ 127|-32,768 ~ 32,767|-21억 ~ 21억|-2^63 ~ 2^63 - 1|소수점 6자리|소수점 15자리|true / false|0 ~ 2^16|

---

### 리터럴 (Literal, Non-Computation-Value)
컴퓨터가 해석하지 않아도 되는 값
|분류|정수형|||||실수형||
|---|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
|종류|10진수|2진수|8진수|16진수	|long 타입|float 타입|double 타입|
|리터럴 값|n|"0b" + n|"0" + n|"0x" + n|	n + "L"|n.n + "F"|n.n|
