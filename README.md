# Jayeong Seo <sub>서자영</sub>

실서비스 운영 경험과 git으로 검증되는 문제 해결 과정을 우선으로 다룹니다.

<sub>Backend Engineer · 이화여자대학교 컴퓨터공학과 2027.02 졸업 예정</sub>

<a href="https://jayeongseo.vercel.app/">Portfolio</a> &nbsp;·&nbsp; <a href="mailto:jayeongseo.kr@gmail.com">jayeongseo.kr@gmail.com</a>

## Selected work

네 개의 서비스를 설계부터 배포·운영까지 맡았습니다. 아키텍처 다이어그램과 트러블슈팅 전문은 <a href="https://jayeongseo.vercel.app/projects">포트폴리오 상세</a>에 있습니다.

### EZBooth

행사·전시 부스 디자인의 3D 모델과 견적서(RFP)까지 자동으로 출력하는 AI 서비스.

- 벤더가 교체돼도 상위 서비스가 영향받지 않는 9모듈 헥사고날 경계
- PortOne 웹훅 HMAC-SHA256 서명 검증과 webhook-id 멱등 가드
- 비관적 락으로 크레딧 read-modify-write 중복 차감 차단
- Hibernate 드라이버 타입 바인딩 버그를 TRACE 로깅으로 특정해 매핑 우회

`Java` `Spring Boot` `Hibernate/JPA` `MySQL` `Docker`

<sub><a href="https://jayeongseo.vercel.app/projects/ezbooth">Case Study →</a></sub>

### EZDocent

관람객과 다국어로 실시간 소통하는 AI 아바타 키오스크. 미국, 스페인 등의 전시 현장에서 실제로 운영됐습니다.

- 컬럼 추가 없이 언어 개수 변경에 대응하는 JSONB 다국어 모델링
- 현장에서 발생한 커넥션 풀 고갈을 max-lifetime과 재시도로 안정화
- Gradle 의존 선언만으로 3모듈 계층의 의존 방향을 단방향 고정
- Discord 임베드 알림 구조화와 정상 연결 종료 오탐 억제

`Java` `Spring Boot` `PostgreSQL` `Supabase` `Render`

<sub><a href="https://jayeongseo.vercel.app/projects/ezdocent">Case Study →</a></sub>

### GLLO

해외에 거주하는 한국인을 위한 다중 통화 가계부. 여러 나라 통화를 한곳에서 관리하고 환율 변동 손익까지 자동으로 계산합니다.

- 내부 도메인부터 실행 모듈까지 단방향 의존성을 지키는 8모듈 헥사고날 경계
- 이동평균법 환율 평단가를 불변 record 도메인 메서드로 구현
- 표준 라이브러리만으로 JWT HS256·ES256 이중 검증과 JWKS 수동 파싱
- 쿼리 조건 축소와 RLS 정책으로 IDOR 이중 차단

`Java` `Spring Boot` `PostgreSQL` `Redis` `Supabase`

<sub><a href="https://jayeongseo.vercel.app/projects/global-ledger">Case Study →</a> &nbsp;·&nbsp; <a href="https://gllo.onrender.com/">gllo.onrender.com</a></sub>

### 털실과 그레텔

원하는 옷 사진을 올리면 뜨개질 도안을 자동으로 만들어 주는 서비스. 커뮤니티 기능도 함께 제공합니다.

- Spring Boot와 FastAPI를 별도 프로세스로 나눈 polyglot 경계 설계
- subprocess 단계별 계측으로 신체부위 분리 병목을 규명
- 대표색 추출·외곽 판정 재작성으로 도안 생성 시간 7배, 10.5배 단축
- 게시글 N+1을 postId IN 배치 조회와 fetch join 조립으로 상수 쿼리화

`Java` `Spring Boot` `FastAPI` `Python` `MySQL`

<sub><a href="https://jayeongseo.vercel.app/projects/knittinggirls">Case Study →</a></sub>

## Also

**Web Swing Simulator** - 웹캠으로 손 동작을 인식해 조작하는 1인칭 3D 웹게임. 웹캠 입력부터 렌더링까지 한 프레임에서 처리하는 단일 파이프라인, One Euro Filter 기반 랜드마크 지터 스무딩, 그리드 해시맵 공간 분할 충돌 판정을 직접 구현했습니다. `TypeScript` `Three.js`<br>
<sub><a href="https://jayeongseo.vercel.app/projects/web-swing">Case Study →</a> &nbsp;·&nbsp; <a href="https://web-swing.vercel.app/">web-swing.vercel.app</a></sub>

**매난국죽** - 사군자와 사계절 컨셉을 결합한 탑다운 서바이벌 어드벤처. 5인 팀이 3일 만에 만든 해커톤 결과물로, 레벨 디자인과 몬스터 조준 로직(이동용 4방향 스냅과 조준용 atan2 연속각 분리)을 맡았습니다. `Unity` `C#`<br>
<sub><a href="https://jayeongseo.vercel.app/projects/mngj">Case Study →</a> &nbsp;·&nbsp; <a href="https://mistywillow.itch.io/mngj">itch.io</a></sub>

**ECHub** - 이화여대 주변 카페를 지도와 카드 리스트로 보여 주는 서비스. SecurityFilterChain 재설계로 web.ignoring 필터 우회를 해결하고, 요일별 영업시간 1:N과 해시태그 M:N 정규화 스키마를 설계했습니다. `Java` `Spring Boot` `Spring Security` `MySQL`<br>
<sub><a href="https://jayeongseo.vercel.app/projects/echub">Case Study →</a></sub>

## Timeline

`2024.01` **ECHub** - 이화여대 컴퓨터동아리 ECC 입회 후 처음 진행한 프로젝트. Controller-Service-Repository 3계층을 단독으로 설계하고, `web.ignoring()` 설정으로 인증 정보가 채워지지 않는 장애를 겪으며 Spring Security 필터 체인의 동작 원리를 실전에서 익혔습니다.

`2024.11` **매난국죽** - 이화여대 게임제작동아리 KING에서 주최한 2박 3일 게임 개발 해커톤. 레벨 디자인과 몬스터 조준 로직을 맡았고, NavMeshAgent 코드 리뷰로 좌표계 처리 원리를 스스로 학습했습니다.

`2024.11` **털실과 그레텔** - 이화여대 졸업 프로젝트. 백엔드(커뮤니티·인증)를 단독 설계하고 DeepLabV3+, SCHP 등 AI 모델 통합과 도안 생성 파이프라인 성능 개선을 담당했습니다.

`2025.11` **EZBooth · EZDocent** - Interexpo Backend CTO로 두 서비스를 동시에 담당했습니다. 벤더 전환에도 포트·어댑터 경계만 바꾸는 구조를 설계했고, 실제 전시 현장에서 발생한 장애를 실시간으로 대응했습니다.

`2026.02` **GLLO** - 독일 교환학생 기간 동안 직접 쓸 다중 통화 가계부가 필요해 설계부터 배포·운영까지 혼자 진행했습니다. 환율 평단가 계산, JWT 이중 서명 검증, IDOR 취약점 자가 발견·수정까지 실사용 중 발생한 문제를 스스로 해결했습니다.

`2026.09` **Web Swing Simulator** - 3D 렌더링 경험을 쌓기 위해 짧은 기간 안에 Three.js 기반 1인칭 웹게임을 제작했습니다. 렌더링 파이프라인 전 구간을 직접 구현했습니다.

`next` **다음** - 이 경험들을 이어갈 다음 자리를 찾고 있습니다.

## Toolkit

<sub>LANGUAGE</sub><br>
`Java` `Python` `TypeScript`

<sub>BACKEND</sub><br>
`Spring Boot` `Spring Security` `JPA/Hibernate` `FastAPI`

<sub>DATABASE</sub><br>
`MySQL` `PostgreSQL` `Redis`

<sub>INFRA</sub><br>
`AWS` `Supabase` `Render` `Netlify`

## Background

<sub>EDUCATION</sub><br>
이화여자대학교 컴퓨터공학과, 2027.02 졸업 예정 · 학점 4.22 / 4.5

<sub>AWARDS</sub><br>
2025 전국 대학생 사회적기업 우수사례발굴 경진대회 은상 - 사회적기업학회<br>
2025 Ewha Engineering Capstone Design Contest 은상 - 이화여자대학교 공학교육혁신센터<br>
2025 창의적 종합설계 경진대회 컨소시엄 우수상 - 고려대학교 공학교육혁신센터<br>
2024 MaKING JAM 5th 우수상 - 교내 게임 개발 해커톤

<sub>ACTIVITY</sub><br>
이화여자대학교 중앙 개발동아리 ECC 2024 회장 - 임기 중 AngelHack-ECC 공식 파트너십 체결, HackSeoul 2024 서포트

<sub>CERTIFICATION</sub><br>
정보처리기사 · SQLD · ADSP · 리눅스마스터 2급 · JLPT N3
