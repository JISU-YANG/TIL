## JAVA 40 LEVEL
# Lv.18 JAVA DOC

### 메뉴얼
작성된 프로그램을 API 문서로 만들어내는 작업을 "메뉴얼을 작성한다."라고 표현한다.

### JAVA DOC
Java 소스 코드에서 HTML 형식의 문서를 생성하기 위한 문서 생성기를 JAVA DOC이라고 한다.
기본적으로 JDK에 javadoc.exe가 포함되어 있다.

### API 주석
API 주석은 /**로 열고 */로 닫혀있다.
작성자, 버전, 매개 변수, 리턴 등 다양한 태그가 사용된다.

### 이클립스 Javadoc 인코딩 설정
이클립스에서 Javadoc을 생성할때 VM 옵션에 UTF-8로 인코딩 타입을 설정해줄 수 있다.
eclipse > export> VM options
-local ko_KR -encoding UTF-8 -charset UTF-8 -docencoding UTF-8