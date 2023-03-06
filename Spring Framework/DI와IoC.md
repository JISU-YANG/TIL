2020.06.29
# DI와 IoC

> DI와 IoC 단어만 들어도 막막하고 거부감부터 드는 개발자들을 위해, 간단하고 쉽게 설명하기 위해 포스팅되었으므로 전문적이고 자세한 내용이 필요하시면 마지막 링크를 보시는 게 더욱 도움되실 겁니다. 개발 지식을 개발자스럽지 않게 설명하겠습니다.

---

개발자가 원하는 순간에 소스코드의 흐름에 맞춰 작동시키는 게 이전의 코딩이었습니다. 하나하나 구체적으로 지목을 해줘야 했고, 이 말은 즉슨 변경 시에도 하나하나 각 파트별로 소스를 다 변경해주어야 했습니다. 이건 번거롭고 불편하고 실수가 생길 수 있는 비효율적인 과정이기 때문에 방법을 고안해냈습니다. 그렇게 DI(Dependency Injection, 의존성 주입)는 탄생했습니다.

---

처음부터 객체를 구체적으로 지목하지 않고 형태만 구성한 후에 사용되는 시점에 객체를 알려주는 겁니다. 구체적인 구현 단계를 절차적으로 나누어 사용되기 전 진행한다고 봐도 무관합니다. 그래서 서비스를 추상화한다고도 이야기합니다. 더욱 바람직한 객체지향적인 프로그래밍인 것이죠.

---

### DI의 장점은 많습니다.
- 객체 간 의존성 관계를 줄여줍니다.
- 코드의 재사용성이 높아집니다.
- 코드의 가독성이 높아집니다.
- 코드의 변화에 유연합니다.

---

### 쉬운 비유는 이렇습니다.

ex 1) 생수(변수)를 마셔라(메소드). 라고 코딩한 후 실행하면 생수(변수)를 마십니다(메소드).

ex 2) 음료(변수)를 마셔라(메소드). 라고 코딩한 후 생수(객체)라는 음료 객체(변수)를 전달한 후 실행하면 생수(변수)를 마십니다(메소드).

</br> 

이렇게 구체적인 객체를 지정하는 게 아니라 실행 단계에서 전달함으로써 코드의 유연성을 가지게 됩니다. 이것을 DI라고 부르게 됩니다.

---

그전에 기본적인 실행하는 주체인 Spring Container (IoC Container, Bean Factory, 이하 컨테이너)가 있습니다. 구체적으로 구현 단계가 분리된 만큼 누군가는 그걸 작동시켜주어야 합니다. 그것을 이 컨테이너가 담당합니다. 개발자가 아니라 컨테이너가 하기 때문에 전문용어로 제어 역전(Inversion of Control)이라는 단어를 사용합니다. 개발자에게 있던 흐름 제어의 주도권이 컨테이너에게 넘어갔다는 의미입니다. 그리고 컨테이너가 작동시킬 수 있도록 준비상태가 되어있게 만드는 것을 의존성 주입(DI)이라고 표현합니다.

---

### Spring Framework에서는 이것을 코드화 하기 위한(의존성 주입) 3가지 방법이 있습니다.
1. 생성자 주입
2. setter 메소드 주입 (or 수정자 주입)
3. 어노테이션 주입 (or 필드 주입)

---

### 예시 코드는 이렇습니다.
1. 생성자 주입

```java
private DependencyA dependencyA;
private DependencyB dependencyB;
private DependencyC dependencyC;

@Autowired
public DI(DependencyA dependencyA, DependencyB dependencyB, DependencyC dependencyC) {
    this.dependencyA = dependencyA;
    this.dependencyB = dependencyB;
    this.dependencyC = dependencyC;
}
```

2. setter 메소드 주입
```java
private DependencyA dependencyA;
private DependencyB dependencyB;
private DependencyC dependencyC;

@Autowired
public void setDependencyA(DependencyA dependencyA) {
    this.dependencyA = dependencyA;
}

@Autowired
public void setDependencyB(DependencyB dependencyB) {
    this.dependencyB = dependencyB;
}

@Autowired
public void setDependencyC(DependencyC dependencyC) {
    this.dependencyC = dependencyC;
```
3. 어노테이션 주입 
```java
@Autowired
private DependencyA dependencyA;

@Autowired
private DependencyB dependencyB;

@Autowired
private DependencyC dependencyC;
```

---

### 실제로 제어 역전을 담당하는 컨테이너의 역할은 꽤나 다양합니다.
따지고 보면 2가지의 컨테이너가 있다고 볼 수 있습니다. 빈 팩토리(Bean Factory)라는 별명을 가지고 있는 컨테이너는 객체를 직접 관리할 수 있고 그 대상을 빈이라고 부릅니다. applicationContext.xml이라는 설정 파일에 등록된 빈을 생성하고 관리하는 거죠. 애플리케이션 콘텍스트(ApplicationContext)라고 불리는 컨테이너는 트랜잭션을 관리하거나 다국어 처리 같은 기능을 지원합니다.

---

### 참조자료
- www.nextree.co.kr/p11247/ 
- asfirstalways.tistory.com/334

