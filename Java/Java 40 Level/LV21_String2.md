## JAVA 40 LEVEL
# Lv.21 String 2, Parsing

### 문자열 나누기
java.lang.String 클래스에 구현되어 있는 대표적인 메소드
- substring()
- split()

### substring() 주의사항
java에서는 end index의 -1로 작동된다.
```java
class Ex(){
    String email = "jisuyang@egoist.im";
    int idx = email.indexOf("@");
    /*
     *       직접 아규먼트를 인덱스로 바인딩하는 경우
     *       exception이 발생하는 것에 주의해야 한다.
     *       탐색을 하는 경우는 index-1을 바인딩하자.
     */
    
    String id = email.substring(0, idx);
    String domain = email.substring(idx + 1);
    String domain2 = email.substring(idx + 1, email.length());
    String etc = email.substring(idx, idx + 1);
    String etc2 = email.substring(100); // Exception
}

```

### split() 주의사항
split(token)에서 주의할 점은 앞에 있는 공백은 포함하지 않고 뒤에 있는 공백은 포함한다.

### StringTokenizer
java.util.StringTokenizer 클래스를 이용하면 iterator 패턴을 사용해 개수와 순서를 모를 때 유리하다.