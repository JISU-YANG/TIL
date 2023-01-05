## JAVA 40 LEVEL
# Lv.1 JDK

### JAVA의 용도

1. 안드로이드(Android) 앱(Application) 개발
2. 홈페이지 및 웹 개발
3. 응용 프로그램 개발 (관리 시스템, 인디게임 등)

---
### JVM, Java Virtual Machine
JAVA 프로그램을 실행한다.
- Class Loader : 메모리 적재
- Runtime Data Areas : 메모리 영역 관리
- Execution Engine : 소스코드를 읽고 실행

---

### JRE, Java Runtime Environment
JAVA 기초 문법 및 클래스를 가지고 있다.
- 운영체제(OS)와 상관없이 실행이 가능
- Server에서는 이것만 요구

---

### JDK, Java Development Kit
JVM과 JRE에 의해 실행되고 구동할 수 있는 자바 프로그램을 생성할 수 있게 한다. 

---

### JDK의 종류별 목적
- ME (Micro)
  임베디드
- SE (Standard)
  jar(실행파일), war(웹)
- EE (Enterprise)
  서버개발

---

### JDK의 버전별 차이 
- 1.6
  - java.util.scanner의 탄생
  - System.out.printf() 바인딩 지원
- 1.7
  - try-catch -> Resource ~ with
  - Switch(정수){} -> Switch(정수 or 문자열)
- 1.8
  - 람다식 표현 (Lambda Expression)

---

### JDK Tools(.jar)
- javac.exe (컴파일러, 자바 소스 파일 -> 바이트 코드)
- javap.exe (클래스 파일 -> 자바 소스코드)
- jdb.exe (디버깅 툴)
- javaDoc.exe (자동 문서 생성)
- javaw.exe (스타트 런처)