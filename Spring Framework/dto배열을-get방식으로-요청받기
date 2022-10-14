# List\<Dto>를 Get 방식으로 서버에 요청받기

## 1/5. 예시 데이터
---
```json
[
    {
        "name": "철수",
        "age": 20
    },
    {
        "name": "영희",
        "age": 20
    }
]
```

## 2/5. Query String으로 변환하기
---
위의 객체 배열을 GET 방식으로 받기 위해 테스트할 Query String으로 작성한다.
__객체명[index].변수명(key)=값(value)__ 형태로 배열 안의 객체의 정보를 입력할 수 있다. ~~구글링을 통해 생각보다 자료가 잘 나오지 않는 것으로 보아 선호하는 방법은 확실히 아닌 것 같다.~~
```
GET
?Profile[0].name=철수&Profile[0].age=20&Profile[1].name=영희&Profile[1].age=20
```




## 3/5. 객체 DTO 만들기
---
Getter, Setter, Constructor가 꼭 필요하기 때문에 Annotation으로 대체한다.
```java
@Data
@NoArgsConstructor
@AllArgsConstructor
public class ProfileDto {
    private String name;
    private int age;
}
```

## 4/5. 객체를 List\<Dto>에 담기
---
객체 배열이라서 Dto를 List에 담아서 전달해야하는데 @RequestParam은 아쉽게도 지원하지 않는다.

-> 그러니 Spring MVC를 사용하기 위해 Wrapper Class를 추가한다. 

```java
@Data
@NoArgsConstructor
@AllArgsConstructor
public class ProfileDtoList {
    private List<ProfileDto> profileDtoList;
}

```


## 5/5. Controller에서 요청받기
---
```java
@GetMapping("/profile")
public void getProfileDtoList(
    ProfileDtoList profileDtoList) {
}
```