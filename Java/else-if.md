### Java
# else if에 관한 고찰

## else if

### else if문
else if는 if문과 함께 쓸 수 있는 범위 조건문이며 if문과 같이 조건식을 정해줄 수 있다.

### 범위 조건문
if문을 다르게 범위 조건문이라고 부르기도 한다. 그 이유는 switch문(선택 조건문)과 다르게 범위를 조건으로 지정해줄 수 있기 때문이다.

```java
int hidden = 3;

if (hidden > 3){
    System.out.println("3보다 높습니다.");
}else if(hidden < 3){
    System.out.println("3보다 작습니다.");
}else{
    System.out.println("3입니다.");
}
```
```java
int hidden = 3;

switch(hidden){
    case 1: System.out.println("1입니다."); break;
    case 2: System.out.println("2입니다."); break;
    case 3: System.out.println("3입니다."); break;
    case 4: System.out.println("4입니다."); break;
    case 5: System.out.println("5입니다."); break;
    default: System.out.println("입니다.");
}
```

## 가독성과 성능
최근 else if문을 기피하고 가독성 향상을 이유로 모두 if문으로 대체하는 개발자를 발견했다. 그래서 조사를 조금 해보았다.

### 기능적 차이
기본적으로 if문을 사용하게 되면, else-if문이나 else문은 수혜를 받게 된다. else문 같은 경우는 조건식에 대한 연산이 작동하지 않는다.
```java
int a = 1;
String result = "";

if(a == 1){
    result = "정답 일치함";
}else{
    result = "정답 일치하지 않음";
}
```
```java
int a = 1;
String result = "";

if(a == 1){
    result = "정답 일치함";
}
if(a != 1){
    result = "정답 일치하지 않음";
}
```

else-if문도 흐름의 수혜를 받는다. if문을 2번 쓰게 되면 항상 두개의 if문의 조건식에 대한 연산이 작동한다. 하지만 else-if문을 사용하게 되면 if문에 해당하는 경우 아래의 else-if문까지 내려가지않는다.

> 범위 조건문이라고 해서 첫번째 if문의 조건식을 제외하고 else-if문의 조건식을 연산하는 것은 아니다.

```java
int arNum = {1,2,3,4};
int cnt = 0;

for(int i = 0; i < arNum.length; i++){
    if(arNum[i] < 0){
        // 첫번째 로직
        cnt++;
    }else if(arNum[i] < 1){
        // 두번째 로직
        cnt++;
    }
}

// cnt = 4;
```

```java
int arNum = {1,2,3,4};
int cnt = 0;

for(int i = 0; i < arNum.length; i++){
    if(arNum[i] < 0){
        // 첫번째 로직
        cnt++;
    }
    if(arNum[i] < 1){
        // 두번째 로직
        cnt++;
    }
}

// cnt = 7;
```

### 속도의 차이
위에서 말한 것과 같이 연산을 덜 하기때문에 else-if가 빨라야 맞다는 추론을 증명하기 위해 직접 측정해보았다. 역시나 결과는 else-if가 빠르다. 혹시나 해서 10번의 결과의 평균으로 비교를 해보아도 결과는 같았다.  

![](/Source/ELSE-IF-%EC%86%8D%EB%8F%84-%EB%B9%84%EA%B5%90.jpeg)

같은 범위 if, if
![](/Source/같은-범위-if-if.png)

같은 범위 if, else-if
![](/Source/같은-범위-if-else-if.png)

다른 범위 if, else-if
![](/Source/다른-범위-if-else-if.png)

다른 범위 if, if
![](/Source/다른-범위-if-if.png)