### Maven

# Plugin과 Dependency의 차이점


> Both plugins and dependencies are Jar files.
>
> But the difference between them is, most of the work in maven is done using plugins; whereas dependency is just a Jar file which will be added to the classpath while executing the tasks.
>
> For example, you use a compiler-plugin to compile the java files. You can't use compiler-plugin as a dependency since that will only add the plugin to the classpath, and will not trigger any compilation. The Jar files to be added to the classpath while compiling the file, will be specified as a dependency.
>
> Same goes with your scenario. You have to use spring-plugin to execute some spring executables [ I'm not sure what spring-plugins are used for. I'm just taking a guess here ]. But you need dependencies to execute those executables. And Junit is tagged under dependency since it is used by surefire-plugin for executing unit-tests.
>
> So, we can say, plugin is a Jar file which executes the task, and dependency is a Jar which provides the class files to execute the task.

위의 [stack overflow](https://stackoverflow.com/questions/11881663/what-is-the-difference-in-maven-between-dependency-and-plugin-tags-in-pom-xml)의 답변을 정리해보았다.


</br>

두 가지 방법 모두 Jar 파일을 클래스 경로에 추가한다. 하지만 용도의 차이점이 있고 완전히 분리된 것이 아니다.


- Dependency
  프로젝트 내부에서 **사용**되기 위한 Class 파일의 Jar 파일을 추가한다. Resource의 개념이다.
- Plugin
  배포 이전의 과정에서 **실행**되는 Class File의 Jar 파일을 추가한다. Tool의 개념이다.


</br>

ex) Junit과 같은 경우,

1. 단위 테스트를 실행하기 위한
2. surefire-plugin에서 사용되는 Jar 파일을
3. 제공하는 Dependency를 추가하게 된다.
