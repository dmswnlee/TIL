# REST API

REST(REpresentational State Transfer)는 HTTP를 기반으로 클라이언트가 서버의 리소스에 접근하는 방식을 규정한 아키텍처이다. 

- HTTP의 장점을 최대한 활용할 수 있고 HTTP 프로토콜을 의도에 맞게 디자인 하도록 유도하고 있다.
- REST의 기본 원칙을 성실히 지킨 서비스 디자인을 **RESTful** 이라고 표현한다.
- **REST API**는 REST를 기반으로 서비스 API를 구현한 것을 의미한다.

<br>

### REST API의 구성

- 자원(resource)
- 행위(verb)
- 표현(representations)

<br>

| 구성 요소 | 내용 | 표현 방법 |
| --- | --- | --- |
| 자원(resource) | 자원 | URI(엔드 포인트) |
| 행위(verb) | 자원에 대한 행위 | HTTP 요청 메서드 |
| 표현(representations) | 자원에 대한 행위의 구체적 내용 | 페이로드 |

<br>

### REST API 설계 원칙

1. URI는 리소스를 표현
- 리소스를 식별할 수 있는 이름은 동사보다 명사를 사용

<br>

2. 리소스에 대한 행위는 HTTP 요청 메서드로 표현한다. 
- HTTP 요청메서드는 클라이언트가 서버에게 요청의 종류와 목적(리소스에 대한 행위)을 알리는 방법
- 리소스에 대한 행위는 URI에 표현하지 않음

<br>

| HTTP 요청 메서드 | 종류 | 목적 | 페이로드 |
| --- | --- | --- | --- |
| GET | index/retrieve | 모든/특정 리소스 취득 | x |
| POST | create | 리소스 생성 | o |
| PUT | replace | 리소스의 전체 교체 | o |
| PATCH | modify | 리소스 일부 수정 | o |
| DELETE | delete | 모든/특정 리소스 삭제 | x |


<br>

### REST API를 통해 응답 받은 status의 종류

| 상태 코드 | 코드 명 | 의미 |
| --- | --- | --- |
| 200 | OK | 요청이 성공적으로 보내졌음을 의미 |
| 201 | Created | 요청이 성공적이였으며 새로운 리소스가 생성되었음을 의미 |
| 400 | Bad Request | 잘못된 문법으로 인하여 서버가 요청을 이해할 수 없음을 의미 |
| 401 | Unathorized | 비인증(Unathorize)된 요청임을 의미 |
| 403 | Forbidden | 콘텐츠에 접근할 권리를 가지고 있지 않음을 의미 |
| 404 | Not Found | 요청받은 리소스를 찾을 수 없음을 의미 |
| 500 | Internal Server Error | 서버가 처리 방법을 모르는 상황을 의미 |