## HTTP 기본 지식
# EP 4. HTTP API 설계

### 클라이언트에서 서버로 데이터를 전송하는 방법은?
크게 두가지가 있다. 쿼리 파라미터(GET)를 통해 전송하거나, 메시지 바디(POST)를 통해 데이터를 전송한다.

### HTTP API 데이터 전송은 언제 사용합니까?
1. 서버 to 서버
2. 앱 클라이언트
3. 웹 클라이언트
4. Content-Type: application/json 주로 사용

### HTTP API로 설계를 할때 URI는?
회원을 예시로 들면 아래와 같다.

> - 회원 **목록** /members -> **GET**
> - 회원 **등록** /members -> **POST**
> - 회원 **조회** /members/{id} -> **GET**
> - 회원 **수정** /members/{id} -> **PATCH, PUT, POST**
> - 회원 **삭제** /members/{id} -> **DELETE**

클라이언트는 등록될 리소스의 URI를 모르기 때문에 서버가 URI 생성하고 관리하며 응답할때 서버가 URI를 반환해주는 것을 컬렉션(Collection)이라고 한다. 위 사진에서는 /members를 말한다.

### 등록을 다룰 때 POST와 PUT의 차이는?

> - 파일 **목록** /files -> **GET**
> - 파일 **조회** /files/{filename} -> **GET**
> - 파일 **등록** /files/{filename} -> **PUT**
> - 파일 **삭제** /files/{filename} -> **DELETE**
> - 파일 **대량 등록** /files -> **POST**

PUT을 사용하는경우는 클라이언트가 리소스 URI(위의 {filename} 부분)를 알고 있어야한다. 클라이언트가 리소스 URI 직접 관리하는 것을 스토어(Store)라고 한다. 위 사진에서는 /files 부분이다.

### HTML FORM을 사용하면 GET과 POST밖에 지원하지 않는데?

> - 회원 목록 /members -> GET
> - 회원 등록 폼 /members/new -> GET
> - 회원 등록 /members/new, /members -> POST
> - 회원 조회 /members/{id} -> GET
> - 회원 수정 폼 /members/{id}/edit -> GET
> - 회원 수정 /members/{id}/edit, /members/{id} -> POST
> - 회원 삭제 /members/{id}/delete -> POST

GET, POST만 지원하면 제약이 생기는데 그것을 해결하기 위해 컨트롤 URI를 사용한다. 위 사진에서 /new, /edit, /delete가 그렇다. 하지만 최대한 Resource 중심으로 설계한 뒤 어쩔 수 없을때 사용한다. 사용하게 될때는 동사를 사용한다.