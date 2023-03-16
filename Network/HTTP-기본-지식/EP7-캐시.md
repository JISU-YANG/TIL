## HTTP 기본 지식
# EP 7. 캐시(Cache)

### 왜 캐시를 사용해야 하는가?
- 캐시 덕분에 캐시 가능 시간 동안 네트워크를 사용하지 않아도 된다.
- 비싼 네트워크 사용량을 줄일 수 있다.
- 브라우저 로딩 속도가 매우 빨라진다.
- 빠른 사용자 경험을 제공한다.

### 캐시 유효시간이 끝나면 무조건 새로 받아와야 하나?
캐시 유효 시간이 초과해도 서버의 데이터가 갱신되지 않으면 304 Not Modified + 헤더 메타 정보(Only Head)로 응답할 수 있다. 클라이언트는 서버가 보낸 응답 헤더 정보로 캐시의 메타 정보를 갱신하여 캐시가 저장하고 있는 데이터를 재활용한다. 결과적으로 네트워크 다운로드가 발생하지만 용량이 적은 헤더 정보만 다운로드하므로 매우 실용적인 해결책이다.

### 검증 헤더와 조건부 요청 헤더는?
- 검증 헤더
    - 캐시 데이터와 서버 데이터가 같은지 검증하는 데이터
    - Last-Modified(요청 파일의 최종 수정시간), ETag(Entity Tag)
- 조건부 요청 헤더
    - 검증 헤더로 조건에 따른 분기
    - If-Mo dified-Since(만료기간이 지나서 새로 Load): Last-Modified 사용
    - If-None-Match(컨텐츠가 변경되었다면): ETag 사용
    - 조건이 만족하면 200 OK
    - 조건이 만족하지 않으면 304 Not Modified

### Entity Tag란?
캐시용 데이터에 임의의 고유한 버전 이름을 달아둔다. (ex) v1.0, asdfqwer) 단순하게 ETag만 확인해서 같으면 유지, 다르면 다시 받는다. 캐시 제어 로직을 서버에서 완전히 관리한다. 

### 캐시 제어 헤더의 종류?
- Cache -Control  
캐시 지시어(directives, 권장)
- Pragma  
캐시 제어(하위 호환)
- Expires  
캐시 유효기간(하위 호환)

### 캐시 지시어의 종류는?
- Cache-Control: max-age  
캐시 유효 시간, 초 단위
- Cache-Control: no-cache  
데이터는 캐시 해도 되지만, 항상 원래(origin) 서버에 검증하고 사용
- Cache-Control: no-store  
데이터에 민감한 정보가 있으므로 저장하면 안 됨
(메모리에서 사용하고 최대한 빨리 삭제)

### 프록시 캐시 서버

- Cache-Control: public  
응답이 public 캐시에 저장되어도 됨
- Cache-Control: private  
응답이 해당 사용자만을 위한 것임, private 캐시에 저장해야 함(기본값)
- Cache-Control: s-maxage  
프록시 캐시에만 적용되는 유효시간
- Age: 60 (HTTP 헤더)  
오리진 서버에서 응답 후 프록시 캐시 내에 머문 시간(초)

### 확실한 캐시 무효화 응답
Cache-Control: no-cache, no-store, must-revalidate
Pragma: no-cache  
오리진 서버와 네트워크 단절 시 오래된 데이터도 보이지 않으며 항상 오류가 나며 매번 검증을 받아야 한다.

### 프록시 캐시 서버
Origin 서버와 클라이언트 사이의 트래픽을 효율적으로 다루기 위해 캐시를 이용한 서버

![](/Source/proxy.png)