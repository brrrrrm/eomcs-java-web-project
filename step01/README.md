# step01 - 웹 애플리케이션 프로젝트의 디렉토리
이 단계에서는 웹애플리케이션 프로젝트의 소스 파일과 설정 파일 등을 보관하고 관리할 디렉토리를 준비한다. 실무에서 널리 사용되는 `메이븐` 표준 디렉토리 구조로 만든다. 메이븐 표준 디렉토리 구조는 특정 개발 도구(예: `이클립스`나 `인텔리제이`, `넷빈즈` 등)에 종속되지 않으며 `전자정부 표준프레임워크`에서도 기본으로 사용하는 디렉토리 구조이다. `안드로이드 스튜디오`의 기본 빌드 도구인 `그레이들`에서도 이 디렉토리 구조를 기본으로 사용하고 있다.

```
메이븐(Maven) - 프로젝트 빌드 도구
이클립스(Eclipse) - 통합 개발 환경
인텔리제이(IntelliJ) - 통합 개발 환경
넷빈즈(NetBeans) - 통합 개발 환경
통합 개발 환경(IDE;Integrated Development Environment) - 개발에 관련된 모든 작업을 지원하는 프로그램
안드로이드 스튜디오(Android Studio) - 안드로이드 앱 개발에 사용하는 통합 개발 환경
그레이들(Gradle) - 프로젝트 빌드 도구
```



## 학습 목표
이 단계를 마치면 다음을 할 수 있어야 한다.
- 메이븐 및 그레이들 프로젝트의 기본 디렉토리 구조를 이해하고 만들 수 있다.

## 필요 기술 및 도구
이 단계를 수행하려면 다음의 기술과 도구가 필요하다.
- 명령창(Windows) 또는 터미널(macOS, Linux), 파일 탐색기(Windows)

## 실습

### 1. 작업 디렉토리 생성
`작업 디렉토리`는 각 단계 별 프로젝트를 보관할 디렉토리이다. 사용자 홈 디렉토리에 `workspace`라는 작업 디렉토리를 만들어 보자. 운영체제에 로그인 한 사용자 아이디가 `eomcs`이라고 가정한다면, 작업 디렉토리의 경로는 다음과 같다.
- Windows: `C:\Users\eomcs\workspace`
- macOS, Linux: `/Users/eomcs/workspace`

다음은 `명령창`을 통해 디렉토리를 만드는 예이다. 명령창 대신 `파일 탐색기`를 사용해도 된다.
```
c:\Users\eomcs> mkdir workspace
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
