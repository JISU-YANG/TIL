# 유지보수와 리팩토링
## EP 4. 코드는 한 번만 작성하라

> 코드를 복사하지 않는다.

코드 클론(code clone) 또는 사본(duplicate)은 발 빠른 수확처럼 느껴지지만 심각한 문제이다. 후에 버그가 발견되었을 경우 모두 고쳐야하는데 비효율적이다. 이미 구현한 메서드를 재사용하거나, 기존 메서드를 좀 더 일반화하면 된다.

<br>

보통 6라인 이상의 코드가 동일할 때 사본/코드 클론으로 간주한다.

* 복사한 코드는 분석하기 어렵다. 다른 사본이 어디있는지 모두 몇 개인지 알수 없는 근본적인 문제가 있다.
* 복사한 코드는 고치기 어렵다. 회귀 버그(regression bug)의 원흉이다.


### 해결방안
* 복사, 붙여넣기 대신 메서드 호출 리팩토링 기법을 사용한다.
* 추출한 메서드를 유틸리티 클래스의 메서드로 만든다.
* 공통된 기능을 묶은 상위 클래스를 상속하여 재정의(Override)해 상위 클래스 추출(Extract Superlass)을 한다.

<br>


* 차라리 복사 대신 기능을 임포트해라.
* 복사한 뒤 고쳐써야하는 경우 위의 상위 클래스 추출을 이용한다.
* 코드는 항상 변할 수 있다.
* 백업 차원의 사본을 뜨는 것보다 차라리 SVN이나 깃 등 버전 관리 시스템을 이용해라.
* 긴 SQL 쿼리나 XML, HTML 문서를 문자열 리터럴 형태로 포함한 코드는 문자열 결합, 파라미터를 사용한 메서드로 추출하여 변형된 문자열을 다루거나 HTML 코드를 만들어주는 템플릿 엔진을 사용한다.
