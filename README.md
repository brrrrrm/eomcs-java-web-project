# eomcs-java-web-project
이곳은 [엄진영의 코딩스쿨]에서 강의하는 자바 웹 애플리케이션 프로젝트의 소스 파일을 보관하는 저장소이다. 한 개의 프로젝트를 `step01`, `step02` 방식으로 단계별로 진행하면서 자바 웹 프로그래밍의 기술을 익힐 수 있도록 구성하였다.

## 대상자
- 자바 기본문법을 학습한 사람
- 서블릿/JSP를 학습하였거나 학습하려는 사람
- 스프링 프레임워크 기반 프로젝트에 참여중이거나 참여할 예정인 사람
- 자바 웹애플리케이션 프로젝트의 유지보수를 맡고 있거나 맡을 예정인 사람

## 목표
- 자바 웹 애플리케이션 개발 방법을 배우고 익히기
- 웹 애플리케이션 개발에 사용되는 다양한 기술의 적용 방법을 배우기
- 과거에서 최근까지 웹 애플리케이션의 구조가 변화되고 발전되는 과정을 경험하기
- 다양한 구조의 웹 애플리케이션을 유지보수 할 수 있는 능력을 갖추기

## 강의 주제
각 단계의 강의 주제는 다음과 같다.

### 프로젝트 준비
#### 기본 이론 - 애플리케이션 아키텍처
- 목표
    - 애플리케이션 아키텍처 종류와 각 아키텍처 별 특징을 이해한다.
- 내용
    - PC 애플리케이션의 아키텍처
    - C/S 애플리케이션의 아키텍처
    - 웹 애플리케이션의 아키텍처
    - 모바일 앱의 아키텍처

#### 기본 이론 - 자바 웹 애플리케이션 아키텍처
- 목표
    - 자바 웹 애플리케이션 아키텍처와 구동 원리를 이해한다.
- 내용
    - 웹서버와 서블릿 컨테이너, 웹 컴포넌트의 관계
    - 클라이언트의 요청을 처리하는 절차

#### step01 - 자바 웹 애플리케이션 프로젝트 준비
- 목표
    - 웹 애플리케이션 프로젝트를 위한 개발 도구를 준비하고 설정할 수 있다.
    - 메이븐 표준 웹 프로젝트 폴더를 생성할 수 있다.
    - 웹 애플리케이션을 서버에 배포하여 실행할 수 있다.
- 내용
    - `그레이들` 빌드 도구를 준비
    - 프로젝트 폴더 생성
    - HTML 페이지 작성
    - 웹 모듈 생성
    - 서블릿 컨테이너 준비
    - 웹 모듈 배치 및 실행
- 구현 기능
    - HTML 시작 페이지 만들기

#### step02 - 이클립스 IDE 사용
- 목표
    - 그레이들을 이용하여 웹 프로젝트를 이클립스 IDE 용으로 설정할 수 있다.
    - 이클립스 IDE로 웹 애플리케이션 프로젝트 다룰 수 있다.
- 내용
    - 그레이들 이클립스 플러그
    - 이클립스 IDE 준비
    - 프로젝트 임포트
    - 서블릿 컨테이너 등록
    - 개발 테스트용 서버 환경 구축
    - 웹 애플리케이션 배치와 실행

### 서블릿
#### step03 - 서블릿 만들기
- 목표
    - 서블릿을 만들 수 있다.
    - 서블릿의 생성과 실행, 소멸 과정을 이해한다.
- 내용
    - Servlet 인터페이스
    - 서블릿의 생명주기
    - 배치 설명서 `web.xml` 파일
    - `@WebServlet` 애노테이션
    - 서블릿을 실행하는 방법
- 구현 기능
    - `수업관리` CRUD 서블릿을 만든다.

#### step03 - GenericServlet 추상클래스의 활용
- 목표
    - GenericServlet 추상클래스의 용도를 이해한다.
    - GenericServlet을 이용하여 서블릿을 만들 수 있다.
- 내용
    - GenericServlet 추상클래스와 Servlet 인터페이스의 관계
    - GenericServlet 추상클래스 상속과 service() 추상메서드
- 구현 기능
    - `수업관리` CRUD 서블릿을 GenericServlet의 서브클래스로 전환한다.
    - `회원관리` CRUD 서블릿을 추가한다.

#### 기본 이론 - HTTP 요청/응답 프로토콜
- 목표
    - 웹 브라우저와 웹 서버 사이에 이루어지는 HTTP 요청과 응답 프로토콜을 이해한다.
- 내용
    - HTTP 요청 프로토콜
    - HTTP 응답 프로토콜

#### step04 - HTTP 응답 콘텐츠 보내기
- 목표
    - 웹 브라우저로 콘텐츠를 출력할 수 있다.
- 내용
    - HTTP 응답과 ServletResponse 객체의 관계
    - 문자열 출력하기
- 구현 기능
    - `수업관리`, `회원관리` 서블릿을 요청했을 때 각 페이지의 제목을 출력한다.

#### step05 - 응답 콘텐츠의 한글 깨짐 현상
- 목표
    - HTTP 응답으로 한글을 출력할 때 한글이 깨지는 이유를 이해한다.
    - HTTP 응답으로 한글 콘텐츠를 출력할 수 있다.
- 내용
    - 문자집합과 인코딩
    - 한글이 깨지는 이유
    - `Content-Type` HTTP 응답 헤더를 설정하는 방법
- 구현 기능
    - `게시물관리` CRUD 서블릿을 추가한다.

#### step06 - 데이터베이스에서 데이터 가져오기
- 목표
    - MySQL DBMS를 설치하고 설정할 수 있다.
    - SQL을 이용하여 테이블 생성과 예제 데이터를 입력할 수 있다.
    - `그레이들`을 이용하여 의존 라이브러리 파일을 자동으로 가져올 수 있다.
    - JDBC와 SQL을 이용하여 DBMS 서버에서 데이터를 가져와 웹 브라우저로 출력할 수 있다.
- 내용
    - DBMS 서버 설치와 설정
    - 테이블 생성과 예제 데이터 입력 SQL
    - `그레이들`을 이용한 의존 라이브러리 관리
    - JDBC 드라이버 준비와 배치
    - SELECT SQL 문과 JDBC 프로그래밍
- 구현 기능
    - `수업 목록/조회`, `회원 목록/조회`, `게시물 목록/조회` 기능을 구현한다.

#### step07 - HTML로 웹 페이지 UI 설계하기
- 목표
    - HTML의 용도를 이해한다.
    - HTML의 주요 태그를 다룰 수 있다.
    - HTML을 이용하여 입력폼을 만들 수 있다.
- 내용
    - HTML 요점 정리
    - 화면 작성에 HTML 적용하기
- 구현 기능
    - `수업 목록/조회`, `회원 목록/조회`, `게시물 목록/조회` 데이터를 HTML 페이지로 출력한다.
    - `수업등록폼`, `회원등록폼`, `게시물등록폼` HTML 페이지를 만든다.

#### step08 - GET 요청 보내기
- 목표
    - GET 방식의 HTTP 요청 프로토콜을 이해한다.
    - GET 방식으로 HTTP 요청을 보내는 다양한 방법을 안다.
- 내용
    - GET 방식 HTTP 요청 프로토콜
    - GET 방식으로 서버에 데이터를 보내는 방법
- 구현 기능
    - `수업 목록` 페이지에서 `<a>` 태그를 이용하여 GET 방식으로 `수업 조회` 페이지를 요청한다.
    - `회원목록`, `게시물목록` 페이지도 마찬가지로 GET 방식을 이용하여 조회 페이지를 요청한다.
    - `수업등록폼` 페이지는 `<form>` 태그를 이용하여 GET 방식으로 등록 서블릿을 요청한다.
    - `회원등록폼`, `게시물등록폼` 페이지도 마찬가지로 form 태그를 이용하여 GET 방식으로 요청한다.       
    - `수업등록`, `회원등록`, `게시물등록` 서블릿을 추가한다.

#### step09 - HTTP 요청 다루기
- 목표
    - 웹 브라우저로부터 받은 데이터를 조회할 수 있다.
- 내용
    - HTTP 요청과 ServletRequest 객체의 관계
    - 요청 파라미터 값 꺼내기
- 구현 기능
    - `수업등록`, `회원등록`, `게시물등록` 서블릿을 추가한다.
    - 입력폼으로부터 받은 값을 확인한다.

#### step10 - GET 요청과 POST 요청
- 목표
    - GET과 POST 요청 프로토콜의 특징을 이해한다.
    - GET과 POST 요청을 이용하여 웹 브라우저에서 웹 서버로 데이터를 보낼 수 있다.
- 내용
    - GET 요청으로 데이터를 보내는 방법
    - POST 요청으로 데이터를 보내는 방법
    - GET과 POST 요청의 특징 및 장단점
    - INSERT/DELETE SQL문을 실행하는 방법
- 구현 기능
    - 목록 페이지에서 GET 방식으로 조회 페이지의 서블릿을 요청한다.
    - 입력폼 페이지에서 POST 방식으로 데이터 등록 서블릿을 요청한다.
    - 입력폼으로부터 받은 데이터를 데이터베이스에 저장한다.
    - `수업삭제`, `회원삭제`, `게시물삭제` 서블릿을 추가한다.

#### step11 - 요청 데이터의 한글 깨짐 처리
- 목표
    - POST 요청으로 전송된 데이터를 읽을 때 한글이 깨지는 이유를 이해한다.
    - POST 요청으로 전송된 한글 데이터를 읽을 수 있다.
- 내용
    - 요청 파라미터 값이 한글일 경우 데이터가 깨지는 이유
    - 한글 파라미터 값을 읽는 방법
    - UPDATE SQL문을 실행하는 방법
- 구현 기능
    - 입력폼의 한글 데이터를 제대로 읽어 데이터베이스에 저장한다.
    - `수업변경`, `회원변경`, `게시물변경` 서블릿을 추가한다.

#### step12 - 리프레시를 이용한 웹 페이지 자동 전환
- 목표
    - 리프레시의 구동 원리를 이해한다.
    - 리프레시를 이용하여 페이지 자동 전환을 구현할 수 있다.
    - HTML 페이지에 리프레시 기능을 삽입할 수 있다.
    - HTTP 응답 헤더를 다룰 수 있다.
    - HTTP 응답 헤더를 이용하여 리프레시를 구현할 수 있다.
- 내용
    - HTML `<meta>` 태그를 이용하여 리프레시를 구현하는 방법
    - HTTP 응답 헤더와
    - HTTP 응답 헤더 `Refresh`를 이용하여 리프레시 구현하는 방법
- 구현 기능
    - 데이터 등록 후 자동으로 목록 페이지로 이동한다.
    - 데이터 변경 후 자동으로 목록 페이지로 이동한다.

#### step13 - 리다이렉트를 이용한 웹 페이지 자동 전환
- 목표
    - 리다이렉트의 구동 원리를 이해한다.
    - 리다이렉터를 이용하여 페이지 자동 전환을 구현할 수 있다.
- 내용
    - HttpServletResponse 객체
    -
- 구현 기능

#### HttpServlet

- `로그인폼` HTML 페이지를 만든다.
- `로그인`을 처리하는 서블릿을 만든다.


### 필터

### 리스너

### JSP

### MVC 아키텍처

### 스프링 IoC 컨테이너

### 스프링 WebMVC

#### step08 - CSS로 웹 페이지 UI 꾸미기
- 목표
- CSS의 용도를 이해한다.
- CSS의 주요 문법을 다룰 수 있다.
- CSS를 이용하여 태그의 모양을 다룰 수 있다.
- 내용
- CSS 요점 정리
- HTML 페이지에 CSS 적용하기
- 구현 기능
- 시작 페이지 `index.html`의 UI 레이아웃을 변경한다.
- 웹 페이지 공통으로 적용할 CSS를 정의하고 적용한다.
