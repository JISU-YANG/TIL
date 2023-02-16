JAVA 40 LEVEL
# Lv.30 Exception

### 용어 별 차이점
- 예외: 작성된 코드의 문제의 유형
- 예시: null point exception
- 처리: 예외가 발생했을대 어떻게 대처할지 정해놓는다. 양이 많더라도 자세히 적는게 중요하다.'
- 유효값: 값의 판단
- 에러 or 오류: 개발자가 처리 불가한 사항

### printStackTrace()
문제를 추적해서 출력해준다.

### JDK 버전별 지원

- 1.6까지: multi catch
- 1.7: or 절 지원
- 1.8: Try ~ Resource ~ with

### Try Catch문
```java
class ex(){
    public static void main(String[] args) {
        try{
            // 감시할 코드
        }catch(Exception1 e1){
            // 파라미터 타입에 해당하는 예외가 발생했을 경우 작동될 코드
        }finally{
            // 선택적으로 사용하며 정리 코드를 주로 작성한다.
        }
    }
}
```
