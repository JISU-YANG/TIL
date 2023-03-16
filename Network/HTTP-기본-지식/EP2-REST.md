## HTTP 기본 지식
# EP 2. REST

### URL, URN, URI의 차이점은?
URL은 자원의 주소(Resource Locator)를 뜻하며 익숙하게 볼 수 있다. URN은 자원의 이름(Resource Name)인데 직관적이지 못해 보편화 되지 못하였다. URI는 이 두가지를 모두 포함한다. 표준 형식은 다음과 같다.
scheme://[userinfo@]host[:port][/path][?query][#fragment]

### 웹 브라우저의 연결 흐름은?
1. 웹 브라우저가 전송될 HTTP메시지를 생성한다.
2. SOCKET 라이브러리를 통해 TCP/UDP에 전달한다.

### HTTP에 유리한 구조는?
클라이언트는 UXUI, 서버는 비즈니스 로직을. 이렇게 각각 담당으로 분리하게 되면 호환성을 위해 다른 환경을 지원하게 될때도, 급격한 트래픽을 위해 서버를 증설할때도 더 효율적으로 관리가 가능하다. Stateless에 대한 이야기이지만 핵심은 서버와 클라이언트는 독립적으로 구분하는 것이 유리하다.

### STATE의 종류?
Stateful은 이전 상태를 보존하고 있어 상태유지라고 하고 Stateless는 필요할 때만 연결을 하여 무상태라고 한다. Stateless의 장점이 더 많다. 갑자기 클라이언트의 요청이 증가해도 서버를 스케일 아웃(수평 확장)하기 용이하고 응답 서버를 쉽게 바꿀 수도 있다. 단점은 매번 요청, 응답하기 때문에 데이터 전송량이 늘어난다. 불가피하게 stateful을 사용해야만 하는 경우가 있지만 최소한으로 사용하도록 해야한다.

### STATELESS의 특징은?
이런 비연결성은 1. http의 기본 모델이고 2. 초 단위 이하의 빠른 응답속도를 가지며 3. 서버 자원을 효율적으로 사용할 수 있다. 단점으로는 1. 매번 TCP/IP 연결을 새로 맺어야 하기 때문에 3 way handshake 시간이 추가된다. 2. 수 많은 자원이 함께 다운로드 된다. 3. 지금은 http 지속연결(Persistent Connections)로 문제가 해결되었다.

### HTTP MESSAGE란?
HTTP 메시지에는 거의 모든 것을 전송할 수 있다. html, text, 이미지, 비디오, 음성, 파일, json, xml 등 다양한 파일을 전송할 수 있다. 서버간의 데이터를 주고 받을 때도 대부분 HTTP를 사용한다.

### HTTP MESSAGE의 구조는?
Start-Line, Header, Empty-Line(CRLF), Message-Body로 구성되어있다. Start-Line은 Request-Line과 Status-Line으로 나뉘는데, Request-Line의 시작라인에는 GET, POST, PUT, DELETE 메서드가 있고 요청대상은 보통 절대경로로 시작한다. HTTP 버전으로 마무리한다. Status-Line은 HTTP 버전으로 시작하여 상태코드를 담는다. 예를들어 200은 성공, 400은 클라이언트 오류, 500은 서버오류이다. Header 부분에는 HTTP 전송에 필요한 모든 부가정보를 담는다. 바디의 설명, 크기, 압축, 인증, 브라우저 요청정보, 서버 정보, 캐시 관리 정보 등이 있다.