# nhahan.github.io

# 서버
서버는 클라이언트에게 네트워크를 통해 정보나 서비스를 제공하는 컴퓨터 시스템으로 프로그램 또는 장치(컴퓨터)를 의미


<br/>
* * * 
<br/>


# 클라이언트
서버에 정보를 요청하고, 그 결과를 사용자에게 전달하는 것


<br/>
* * * 
<br/>


# HTTP란?
HTTP(Hypertext Transfer Protocol)하이퍼텍스트 전송 규약. 웹 브라우저(web browser) 같은 응용프로그램을 통해 웹 클라이언트(사용자)와 웹 서버(서비스 제공자) 사이 데이터를 전송하는 프로토콜이다.


<br/>
* * * 
<br/>


## 프로토콜(Protocol)이란? 
프로토콜은 컴퓨터나 네트워크 장비가 서로 통신하기 위해 미리 정해 놓은 약속, 규약이다.


<br/>
* * * 
<br/>


![](https://images.velog.io/images/kisy324/post/b47ae4bf-ad7c-453c-b74f-d742b8a28544/fafzfb.png)

## HTTP 상태코드
- 1xx: Informational - 요청 정보 처리 중
- 2xx: Success - 요청을 정상적으로 처리함
- 3xx: Redirection - 요청을 완료하기 위해 추가 동작 필요
- 4xx: Client Error - 서버가 요청을 이해하지 못함
- 5xx: Server Error - 서버가 요청 처리 실패함


<br/>
* * * 
<br/>


## HTTP Method
- GET - 정보 검색 ex) 게시판 리스트 불러오기
- POST - 실행 / 저장 ex) 회원가입 / 로그인
- PUT - 전체 수정 ex) 회원정보 전체 수정
- DELETE - 삭제 ex) 회원정보 삭제
- PATCH - 일부 수정 ex) 회원정보 일부 수정 (Update에 가장 가깝게 쓰이고 있다)
- OPTIONS - 시스템에서 지원하는 메소드 확인


<br/>
* * * 
<br/>


## HTTP server종류
- Apache HTTP Server
- Tomcat < 스프링 관련해서 보면 거의 톰캣만 언급이 되던데...
- IIS
- Weblogic
- Web sphere


<br/>
* * * 
<br/>


![](https://images.velog.io/images/kisy324/post/93db07e7-d1fa-4302-acc8-cd4270a4b867/restful.png)


# REST(Representational State Transfer):자원의 상태 전달 - 네트워크 아키텍쳐

1. 클라이언트와 서버가 서로 독립적으로 분리되어 있어야 한다.
2. 요청에 대해서 클라이언트의 상태를 서버에 저장하지 않는다.
3. 클라이언트는 서버의 응답을 Cache(임시저장)할 수 있어야 한다. 클라이언트가 Cache를 통해서 응답을 재사용할 수 있어야 하며, 이를 통해 서버의 부하를 낮춘다.
4. 서버와 클라이언트 사이에, 방화벽, 게이트웨이, Proxy 등 다양한 계층 형태로 구성이 가능해야 하며, 확장할 수 있어야 한다.
5. 인터페이스의 일관성을 지키고, 아키텍쳐를 단순화시켜 작은 단위로 분리하여 클라이언트와 서버가 독립적으로 개선 될 수 있어야 한다.
6. 자바 애플릿, 자바스크립트, 플래시 등 특정한 기능을 서버로부터 클라이언트가 전달받아 코드를 실행 할 수 있어야 한다.


<br/>
* * * 
<br/>


## 인터페이스의 일관성
- **자원의 식별**
웹 기반의 REST에서는 리소스 접근을 할 때 URI를 사용한다.
ex)https://foo.co.kr/user/100
Resouce는 user, 식별자는 100

- **메시지를 통한 리소스 조작**
HTML, XML, JSON, TEXT 등의 데이터 타입을 HTTP Header부분의 content-type을 통해서 지정해준다.

- **자기서술적 메시지**
요청하는 데이터가 어떻게 처리되어져야 하는지 충분한 데이터를 포함 할 수 있어야 한다.
GET, POST, PUT, DELETE

- **Application 상태에 대한 엔진으로써 하이퍼미디어**
REST API를 개발할 때 단순히 Client 요청에 대한 데이터만 응답해주는 것이 아닌 관련된 리소스에 대한 Link 정보까지 같이 포함되어져야 한다.

