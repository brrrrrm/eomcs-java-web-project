# step01

- 글로벌 표준에 맞춰 웹애플리케이션 프로젝트의 디렉토리를 준비하라.

이 단계에서는 웹애플리케이션 프로젝트의 소스 파일과 설정 파일 등을 보관하고 관리할 디렉토리를 준비할 것이다. 실무에서 널리 사용되는 방식으로, 특정 IDE(Eclipse, IntelliJ, NetBeans 등)에 종속되지 않으며 Maven이나 Gradle 빌드 도구에서 기본으로 사용하는 디렉토리 구조이다. 대다수의 오픈 소스 프로젝트나 실무 프로젝트가 이 구조로 되어 있다.


## 학습목표
이 단계를 마치면 다음을 할 수 있어야 한다.
- Maven 및 Gradle 프로젝트의 기본 디렉토리 구조를 이해하고 만들 수 있다.

## 필요 기술 및 도구
이 단계를 수행하는 데 필요한 기술이나 도구는 다음과 같다.
- 명령창(Windows) 또는 터미널(macOS, Linux)
- 파일 탐색기(Windows)를 사용해도 된다. 

## 실습

### 1. 작업 디렉토리 생성하기
`작업 디렉토리`는 각 단계 별 프로젝트를 보관할 디렉토리이다. 사용자 홈 디렉토리에 `study-workspace`라는 작업 디렉토리를 만들어 보자. 운영체제에 로그인 한 사용자 아이디가 `eomcs`이라고 가정한다면, 작업 디렉토리의 경로는 다음과 같다.
- Windows: `C:\Users\eomcs\study-workspace`
- macOS, Linux: `/Users/eomcs/study-workspace`

디렉토리를 만들 때 다음과 같이 `명령창`을 사용해도 되고, 또는 `파일 탐색기`를 사용해도 된다.
```
c:\Users\eomcs> mkdir study-workspace
```

### 2. 프로젝트 디렉토리 생성하기
작업 디렉토리에 `step01` 프로젝트에서 사용할 디렉토리를 생성한다.
```
c:\Users\eomcs> cd study-workspace
c:\Users\eomcs\study-workspace> mkdir step01
```
 
### 3. 소스 디렉토리 생성하기 
`step01` 프로젝트의 소스 파일이나 설정 파일 등을 저장할 디렉토리를 생성한다.
```
c:\Users\eomcs\study-workspace> cd step01
c:\Users\eomcs\study-workspace\step01> mkdir src            - 소스 디렉토리 생성
c:\Users\eomcs\study-workspace\step01> cd src               - src 디렉토리로 이동
c:\Users\eomcs\study-workspace\step01\src> mkdir main       - src 안에 main 디렉토리 생성
c:\Users\eomcs\study-workspace\step01\src> cd main          - main 디렉토리로 이동
c:\Users\eomcs\study-workspace\step01\src\main> mkdir java  - main 안에 자바소스 디렉토리 생성
c:\Users\eomcs\study-workspace\step01\src\main> mkdir resources  - main 안에 기타파일 디렉토리 생성
c:\Users\eomcs\study-workspace\step01\src\main> mkdir webapp  - main 안에 웹파일 디렉토리 생성
c:\Users\eomcs\study-workspace\step01\src\main> cd ..       - 상위의 src 디렉토리로 이동
c:\Users\eomcs\study-workspace\step01\src> mkdir test       - src 안에 테스트 소스 디렉토리 생성
c:\Users\eomcs\study-workspace\step01\src> cd test          - test 디렉토리로 이동
c:\Users\eomcs\study-workspace\step01\src\test> mkdir java  - test 안에 자바소스 디렉토리 생성
c:\Users\eomcs\study-workspace\step01\src\test> mkdir resources  - test 안에 기타파일 디렉토리 생성
```

위의 명령을 통해 생성한 디렉토리 구조는 다음과 같다.
```
step01
|--- src
    |--- main
        |--- java
        |--- resources
        |--- webapp
    |--- test
        |--- java
        |--- resources
```  
- main 
    - 프로그램 실행 자바소스파일 및 그와 관련된 파일을 두는 디렉토리다.
- main/java
    - 자바 소스 파일을 두는 디렉토리다.
    - 예) Hello.java 등
- main/resources
    - 프로그램에서 사용할 설정 파일 등을 두는 디렉토리다.
    - 예) jdbc.properties, application-context.xml, MemberMapper.xml 등
- main/webapp
    - HTML, CSS, JavaScript, JSP, GIF 등 웹관련 파일을 두는 디렉토리다.
    - 예) index.html, common.css, jquery.js, list.jsp, photo.gif 등
- test 
    - 단위 테스트 관련 자바소스파일 및 그와 관련된 파일을 두는 디렉토리다.
- test/java
    - 단위 테스트를 실행하는 자바 소스 파일을 두는 디렉토리다.
- test/resources
    - 단위 테스트에 사용할 설정 파일 등을 두는 디렉토리다.
