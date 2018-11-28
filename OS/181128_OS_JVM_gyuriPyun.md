# JVM 이란?
Java Virtual Machine의 줄임말. JVM은 Java Byte Code를 OS에 맞게 해석해주는 역할을 한다. Java compiler는 .java파일을 .class라는 Java Byte Code로 변환시켜 준다. Byte Code 자체는 기계어가 아니기 때문에 OS에서 바로 실행될 수 없다. 이 때 JVM이 OS가 Byte Code 를 이해할 수 있도록 해석해준다.


JVM은 Byte Code를 어느 플랫폼에서나 동일한 형태로 실행시킨다. 때문에 자바로 개발된 프로그램은 CPU나 OS의 종류에 관계없이 JVM을 설치할 수 있는 시스템에서는 어디서나 실행할 수 있다!

여기서 규리가 모르는 것.


#### Java Byte Code
Java Byte Code는 JVM이 실행하는 명령어 집합이다. 컴파일하면 생성되는 .class 파일이 byte code를 담고 있어요.
<이미지 1>

#### JRE (Java Run Environment)
Java 파일 실행을 위한 환경. JVM이 실행되도록 도와주는 역할을 한다. JVM이 자바 프로그램을 동작시킬 때 필요한 library file들과 기타 file들을 가지고 있다. JRE는 JVM의 실행환경을 구현한 것이라고 할 수 있다. 자바 개발이 필요 없고 실행만을 원한다면 JRE만 설치하면 됨.

<img src = "https://user-images.githubusercontent.com/26535709/49169050-4857ad80-f37c-11e8-89e0-2beb6b092225.jpg" width = 50%>

#### JDK (Java Development Kit)
말 그대로 자바 개발을 위한 도구(Kit)이다. 자바 컴파일러(Javac), 자바가상머신(JVM) 등 각종 Java Library 등을 포함하고 있어 자바 개발을 위한 필수 Kit이다! JDK는 JRE를 포함하고 있어요. (JDK설치하면 JRE도 설치됨)

<img src = "https://user-images.githubusercontent.com/26535709/49169051-4857ad80-f37c-11e8-8350-7b2faf63ae6a.jpg" width = 50%>




### Java Compiler
.javac (자바 소스 코드)를 .class (Byte Code)로 변환한다.

### Class Loader
Java는 class를 동적으로 읽어온다. 즉, runtime에 모든 코드가 JVM에 링크된다. 모든 class는 그 class가 참조되는 순간에 동적으로 JVM에 링크되며, 메모리에 로딩된다.
JVM은 compiler time이 아닌 runtime 시에 처음으로

### Runtime Data Areas
runtime data 영역은 JVM이라는 프로그램이 OS 위에서 실행되면서 할당받는 메모리 영역이다. runtime data area는 5개의 area로 나눌 수 있다. 이 중 PC Register, JVM Stack, Natvie Method Stack은 thread마다 하나씩 생성되며 Heap, Method Area는 모든 thread가 공유해서 사용한다.

<img src = "https://user-images.githubusercontent.com/26535709/49169047-47bf1700-f37c-11e8-99e6-e6f53d7fadf1.png" width = 40%>

### Java의 실행 과정
1. User가 Java 코드 생성
2. JDK로 컴파일(.class 파일 생성)
3. JVM을 통해 Java Byte Code로 변환.
4. JRE로 실행

<img src = "https://user-images.githubusercontent.com/26535709/49169049-4857ad80-f37c-11e8-9a62-63df42784253.png" width = 40%>


<출처>
출처가 막 전문적인 사이트가 아니네요...
- 자바, 프로그래밍 언어 http://www.wikiwand.com/ko/자바_(프로그래_언어)
- https://wikidocs.net/257
