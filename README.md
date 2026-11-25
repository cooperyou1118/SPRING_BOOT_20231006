2주차:스프링 부트 개발환경, 테스트 완료
• [index.html : 실행/수정 완료](https://github.com/cooperyou1118/SPRING_BOOT_20231006)

3주차: 부트스트랩5 기반 디자인(네비바, 아이콘, 이미지, 프로필) 변경
       Css, js, image 코드 타임리프 출력방식으로 변경
       기술 상세페이지 연동
       포트폴리오 작성
       
4주차: 스프링 부트와 MySQL 연동 설정
       엔티티 클래스 및 리포지토리 작성
       데이터베이스 조회를 위한 서비스 및 컨트롤러 구현
       타임리프를 활용한 데이터베이스 목록 출력 실습

5주차: Spring Security 의존성 추가 및 보안 설정 구성
       BCrypt를 이용한 비밀번호 암호화
       회원가입 및 로그인·로그아웃 기능 구현
       URL별 접근 권한 설정 및 세션 인증 처리

6주차: Spring Security 권한(ROLE) 설정 및 관리자 페이지 접근 제어
       URL 규칙 및 메서드 수준의 보안 강화(@PreAuthorize)
       403 접근 거부 페이지 구현 및 오류 해결 실습

8주차: REST 및 JSON 기본 개념 학습
       회원 관리 기능의 REST API 전환 구현
       내 정보 및 관리자용 API 컨트롤러 작성(@RestController)
       민감 정보 노출 방지를 위한 응답 DTO(MemberResponse) 적용
       Spring Security를 활용한 API 접근 권한 및 Basic 인증 설정
       회원 등록, 권한 변경, 회원 삭제 API 구현

중간고사 핵심 요약:
1. 2주차: 웹 API와 REST·JSON 개념
       API (Application Programming Interface): 프로그램끼리 데이터를 주고받기 위한 공통의 약속(주문서). 화면(HTML)이 아니라 데이터(JSON)를 주고받는 데 초점을 맞춤.

       서버와 클라이언트 구조: 하나의 백엔드 서버가 웹 브라우저, 모바일 앱, 스마트워치 등 여러 클라이언트에 데이터를 제공할 수 있음.

       REST (Representational State Transfer): API를 설계하는 규칙으로, 주소(URL)는 대상을 나타내고, HTTP 메서드(GET, POST, PATCH, DELETE)는 수행할 작업을 나타냄.

       JSON: 사람이 읽기 쉬운 데이터 표현 형식으로, 객체({})와 배열([]) 형태로 구성됨.

2. 3주차: 포트폴리오 프론트엔드 및 타임리프 레이아웃
       SSR (Server-Side Rendering): 서버(Thymeleaf)에서 HTML 화면을 완성해서 브라우저에 보내는 기존 방식.

       타임리프(Thymeleaf): 스프링 부트에서 HTML 템플릿을 동적으로 렌더링하기 위해 사용하는 템플릿 엔진으로, 공통 레이아웃을 분리하여 관리할 수 있음.

3. 4주차: 데이터베이스 연동과 JPA
       JPA (Java Persistence API): 자바 객체와 데이터베이스 테이블을 매핑해 주는 ORM 기술.

       핵심 계층 구조 (MVC 패턴):

       Entity: DB 테이블과 직접 매핑되는 데이터 객체

       Repository: Spring Data JPA를 상속받아 DB에 접근하는 인터페이스 (CRUD 메서드 제공)

       Service: 비즈니스 로직을 처리하는 계층

       Controller: 사용자의 요청을 받고 응답을 반환하는 계층

4. 5주차: Spring Security 및 인증·암호화
       Spring Security: 웹 애플리케이션의 인증(Authentication)과 인가(Authorization)를 담당하는 보안 프레임워크.

       비밀번호 암호화 (BCrypt): 사용자 비밀번호를 평문으로 저장하지 않고 해시(Hash) 처리하여 안전하게 보관함.

       로그인 / 로그아웃: 세션을 이용해 인증된 사용자의 상태를 유지하고, 로그인 여부에 따라 접근을 제어함.

5. 6주차: 권한 관리와 관리자 페이지
       인가 (Authorization) 및 역할(Role): 사용자마다 권한(USER, ADMIN)을 부여하여 특정 페이지나 기능에 접근할 수 있는지 제어함,

       접근 제어: 시큐리티 설정 파일에서 hasRole("ADMIN") 등을 통해 관리자 전용 URL(/admin/**) 접근을 차단함.
       메서드 보안 (@PreAuthorize): 특정 컨트롤러나 메서드 실행 전에 권한을 검사함.

6. 7주차: REST API 구현 및 상태 코드
       @RestController vs @Controller:

       @Controller: HTML 화면 이름을 반환 (SSR)

       @RestController: 객체를 반환하면 자동으로 JSON으로 변환하여 응답

       응답 DTO (Data Transfer Object): 엔티티를 그대로 반환하면 비밀번호 해시 값 같은 민감한 정보가 노출되므로, 필요한 데이터만 골라서 담는 DTO(MemberResponse)를 만들어 반환함.

       주요 HTTP 상태 코드:

       200 OK: 조회/수정 성공

       201 Created: 새로운 자원 생성 성공 (회원 가입 등)

       204 No Content: 성공했으나 반환할 본문이 없음 (삭제 등)

       400 Bad Request: 잘못된 요청 (필수값 누락, 중복 아이디 등)

       401 Unauthorized: 인증되지 않음 (로그인 정보 없음)

       403 Forbidden: 권한 없음 (일반 유저가 관리자 API 호출)

       404 Not Found: 대상이 존재하지 않음

9주차: 게시판 CRUD와 본인 확인
       게시판 기본 기능 (CRUD): Spring Boot와 JPA를 활용해 게시글 작성(Create), 조회(Read), 수정(Update), 삭제(Delete) 기능 구현.
       JPA 연관관계 매핑 (@ManyToOne): 게시글(Post) 엔티티와 회원(Member) 엔티티를 N:1 다대일 관계(외래 키)로 연결하여 작성자 정보 관리.
       서버 측 작성자 검증 (본인 확인): 수정 및 삭제 작업 시 SecurityContextHolder를 통해 로그인한 사용자 정보와 작성자 정보가 일치하는지 검증하고, 미일치 시 AccessDeniedException(403) 처리.

10주차: 페이징, 검색 및 댓글 기능
       페이징 (Spring Data JPA Pageable): `Pageable` 및 `PageRequest`를 활용하여 10개 단위로 게시글 목록을 나눈 페이징 처리와 SQL `LIMIT`/`OFFSET` 메커니즘 이해.
       JPQL 기반 키워드 검색: `@Query`와 JPQL을 활용해 제목 및 내용에서 검색어를 찾는 파라미터 바인딩 기능 구현 (SQL Injection 방지).
       댓글 기능 및 Cascade 삭제: 게시글과 댓글 간 연관관계(@OneToMany)를 설정하고, 게시글 삭제 시 관련 댓글이 자동 삭제되도록 `CascadeType.REMOVE` 적용 및 POST-Redirect-GET(PRG) 패턴을 이용한 댓글 중복 작성 방지.

11주차: 파일 업로드, 신청 바구니 및 트랜잭션
       모집글 확장 및 포스터 이미지 업로드: 기존 `Post` 엔티티에 정원(`capacity`) 및 신청 인원(`appliedCount`) 필드를 추가하고, `MultipartFile`과 `FileStore`(확장자·매직바이트 검증, UUID 저장) 및 `WebConfig` 정적 리소스 매핑을 적용해 포스터 업로드 구현.
       세션 기반 신청 바구니: `HttpSession`과 `LinkedHashSet`을 활용해 중복 없이 담은 순서를 유지하는 임시 신청 바구니(담기, 빼기, 조회) 구현.
       트랜잭션 관리 (`@Transactional`): 바구니 일괄 신청 확정 시 `Enrollment` 저장 및 모집 인원 차감 로직을 하나의 작업 단위로 묶어, 정원 마감 등 예외 발생 시 전체 작업이 롤백(ACID 원자성)되도록 처리.
       JPA 변경 감지 및 데이터 무결성: 트랜잭션 내 엔티티 상태 변경을 통한 자동 UPDATE(Dirty Checking) 적용, PRG 패턴과 `RedirectAttributes`를 이용한 메시지 전달, 신청 내역이 존재하는 모집글·회원의 무분별한 삭제 방지 처리.

12주차: 12주차: WebSocket 및 STOMP 기반 실시간 알림
       WebSocket 및 STOMP 설정: `spring-boot-starter-websocket` 의존성 추가 및 `WebSocketConfig`를 통해 `/ws` 엔드포인트와 메시지 브로커(`/topic`, `/queue`, `/user`) 구성.
       실시간 남은 자리 브로드캐스팅: Java `record`(`SeatMessage`)와 `SimpMessagingTemplate`을 활용하여 신청 확정 및 취소 시 `/topic/seats` 구독자에게 남은 정원 정보를 새로고침 없이 즉시 전송.
       트랜잭션 이벤트 기반 메시지 발행: `ApplicationEventPublisher`와 `@TransactionalEventListener(AFTER_COMMIT)`를 연동하여 DB 커밋이 완료된 후에만 실시간 메시지를 전송함으로써 롤백 시 유령 메시지 발생 방지.
       1:1 개인 알림 기능 구현: `convertAndSendToUser` 및 `/user/queue/notifications` 경로를 활용해 모집글 작성자에게만 신청·취소·댓글 실시간 알림 전송.