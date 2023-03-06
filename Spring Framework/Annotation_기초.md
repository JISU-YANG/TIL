2019.10.24
# Annotation 기초
### Annotation의 환경
Spring Web Mvc Framework는 java1.5부터 Annotation을 지원한다.

### Annotation의 장점
1. 설정이 간편해진다.
2. view 페이지와 (객체 또는 메소드)의 Mapping이 명확해진다.

### 대표적인 Annotation
- @Component
  - Stereotype의 최상위 Annotation
- @Controller
  - Spring MVC에서 Controller로 인식시켜준다.
- @Service
  - Business Class에서 로직을 사용한다. (Business Layer)
- @Repository
  - DB에 접근하는 클래스임을 명시한다. 일반적으로 DAO에서 사용한다.

### Annotation의 등록 
Stereotype의 Annotation은 **context:component-scan**에 의해 자동으로 등록되어지고 Spring Framework가 관리해준다. 

### Annotation의 종류 
- @Component
- @Autowired
- @Qualifer
- @Required
- @Repository
- @Service 
- @Resource