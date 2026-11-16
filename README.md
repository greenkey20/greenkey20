# Hi, I am Eunyoung 👋

6년간의 금융 실무를 거쳐 개발자로 전환한 **Java · Spring 백엔드 개발자**입니다. (개발 만 3년 차)<br>
국채 트레이딩 시스템과 결제 시스템을 개발해 왔고, 문제를 풀고 데이터를 다루는 일을 좋아합니다. 직접 만들고 배포하며 배웁니다.

📄 **업무 경험과 프로젝트 상세는 [CV (Notion)](https://greenkey20.notion.site/eunyoung-kang)에서 볼 수 있습니다.**

## 💼 Experience

**금융 SI/솔루션 백엔드 개발 · 자본시장사업부 (2023.11 ~ 현재)**

- **Tradegene** ([국채전문유통시장 트레이딩 솔루션](http://www.tradegene.co.kr)) — `Java 17` `Spring Boot 3` `Spring Data JPA` `PostgreSQL` `Kafka` `Redis`
  - 은행 고객사 3곳의 국채전문유통시장 솔루션 프로젝트에서 딜러용 거래 웹앱의 **알고리즘 트레이딩 백엔드**를 담당
  - Hexagonal Architecture + CQRS 구조의 MSA에서 **알고리즘(시그널 이벤트 로그 · 룰 시그널), Risk Management, Portfolio** 서비스와 조회(Query) 서비스를 개발하고, Kafka 이벤트와 FeignClient로 서비스 간 연계
  - **데이터 관리(커스텀) MSA를 부담당**하며, KRX 호가 전문 수신 시 **호가 초 단위 스냅샷과 통계**를 생성해 Redis/DB에 저장
  - 룰 기반 시그널 판단 로직 구현
  - 사내 크립토거래시스템(Tradegene-crypto, 2025.4 ~ 7)에서 Signal MSA를 맡아 실시간 이벤트로 거래 가능 여부 시그널을 발행하고, 원시 시장 데이터 전체 저장의 메모리 부담을 줄이기 위해 **Redis 윈도우 기반 이벤트 버퍼**를 설계 (메모리 사용량 약 80% 절감)
- **CLS 결제 시스템 재구축** (2024.1 ~ 2025.4) — `C (ProFrame)` `Oracle` `JavaScript (XFrame)`
  - 20년 된 레거시 CLS 결제 시스템을 은행의 상품처리시스템 안으로 통합하고, 결제 전문 송수신·결제 대사·지준 처리 업무와 연동
  - 수기로 하던 전문 작성을 없애고, 기능 모듈화로 Phase2 구현 기간 35% 단축
- 팀 협업: 스프린트 회의 발표 템플릿을 제작해 공유, API 문서화

**한국산업은행 · 행원/대리 (2012.2 ~ 2018.4)**

- 외환 및 외화채권 거래 결제, 해외 기업 여신 마케팅·심사(상하이지점 OJT), 국제금융 기획·관리, 국내 기업 여신 심사
- 이 경험으로 금융 거래와 결제 프로세스를 업무 관점에서 이해한 채 개발합니다.

개인적으로는 2022년부터 Notion에 학습·트러블슈팅 **TIL 1,000건 이상**을 꾸준히 기록하고 있습니다.

## 🌐 Web 채널 개발 경험 (Spring MVC · MyBatis · JSP · AJAX)

### 🛒 [SOSOBUTSTRONG(위메샐)](https://github.com/greenkey20/SOSOBUTSTRONG): 판매자·구매자 거래 웹 서비스 (KH정보교육원 팀 프로젝트, 2022.3~4)
`Java` `Spring MVC` `MyBatis` `Oracle` `JSP/JSTL` `jQuery(AJAX)` `Spring Security` `Maven`

구매자와 판매자가 거래하는 웹 서비스를 팀으로 개발했습니다. 저는 **문의(Q&A), 판매자 정산, 공지사항** 기능을 담당했습니다.
- **1:1 문의/답변**: 구매자의 문의 등록·수정·삭제·검색과 판매자의 답변(첨부파일 포함)을 구현하고, 답변이 등록되면 JavaMail로 구매자에게 이메일을 발송했습니다. 답변 평점은 AJAX로 비동기 처리했습니다.
- **주문 연동 AJAX**: 문의 작성 시 구매자의 주문 목록을 페이징 정보와 함께 JSON으로 비동기 조회하고, 주문번호 확인과 판매자명 자동완성 검색을 구현했습니다.
- **판매자 정산**: 오늘의 신규 주문, 배송 상태별 건수, 정산 예정 금액을 집계하는 MyBatis/Oracle SQL을 작성하고(수수료 5% 반영), 새로고침은 AJAX로 처리했습니다. 정산 상세 목록은 페이징하고, Apache POI로 **엑셀 다운로드**를 제공합니다.
- **공지사항**: 관리자 공지 등록·수정과 사용자 목록·상세 조회를 구현했습니다.

### 🗓️ [Alloc(알록)](https://github.com/greenkey20/knou-key-project): 활동 계획 계산기 (기획·개발·배포 1인, 2023.6~8)
`Java 17` `Spring Boot 3.1` `Spring Data JPA` `Spring Security` `JSP/JSTL` `jQuery` `MySQL(AWS RDS)` `AWS EC2` `GitHub Actions` `S3` `CodeDeploy`

목표 기간과 분량을 입력하면 매 회 수행할 분량을 계산해 주고, 일정 저장·수행 트래킹·통계·게시판을 제공하는 웹 서비스입니다. **방송대 컴퓨터과학과 총장배 소프트웨어 경진대회 은상(2023.8)**.
- Spring Boot + JSP/JSTL + jQuery로 화면과 API를 모두 개발하고 Tomcat(WAR)으로 배포
- GitHub Actions로 빌드 후 S3에 올리고 CodeDeploy로 EC2에 배포하는 **CI/CD 파이프라인** 구성
- **OpenAI(ChatGPT) API 연동**: RestTemplate으로 Chat Completions API를 호출해, 구조화된 프롬프트에 따라 공부 계획을 생성하고 응답을 저장

## ⚙️ 백엔드 설계 · 운영 (개인 프로젝트)

### 🪐 [Inner Orbit](https://github.com/greenkey20/inner-orbit): 감정·인사이트 로그 서비스 (백엔드 중심 개인 프로젝트)
`Java 21` `Spring Boot 3.5` `Spring Security` `JPA` `PostgreSQL` `Flyway` `Redis` `Docker Compose` `React`

개발자의 일상·감각·통찰을 구조화해서 기록하고, AI로 패턴을 분석하는 멀티 유저 웹 서비스입니다.
- **헥사고날 아키텍처(Ports & Adapters)** 로 도메인(`auth`, `log`, `ai`, `weeklyreport`)과 외부 기술(JPA·OpenAI·Redis)을 분리
- **JWT 인증/인가**: Spring Security + jjwt, BCrypt 해시, 사용자별 데이터 완전 격리(`users` 테이블 + FK)
- **DB 마이그레이션 운영 규칙**: Flyway(V1~V10)로 스키마 변화를 관리. 커밋된 migration은 수정·삭제하지 않고 새 버전으로 고치는 원칙을 세워 운영 DB와 어긋나지 않게 관리
- **PostgreSQL JSONB**로 모드별(Daily/Sensory/Insight) 데이터 스키마를 분리하고 V5/V6 마이그레이션으로 이전
- **Redis**로 AI 질문 이력을 TTL 30일로 관리해 반복 방지, **`@Scheduled`** 주간 리포트 자동 생성(멱등성 보장)
- **Spring AI**로 OpenAI를 연동하고, 저장 전 분석은 Stateless API로 분리
- Docker Compose(PostgreSQL · Redis · Nginx)로 개발·운영 환경 구성

### 🎵 [song-lingo](https://github.com/greenkey20/song-lingo): 외국어 문장 발음·받아쓰기 연습 서비스 (기획부터 배포까지 1인 개발)
`Python` `Streamlit` `faster-whisper` `PostgreSQL` `Oracle Cloud` `Cloudflare Tunnel`

듣고 따라읽거나 받아쓰면 STT로 인식해 오류율(WER/CER)과 틀린 부분을 알려주는 음성 학습 앱입니다. **https://songlingo.kr** 에서 실제로 운영 중입니다.
- 로그인(scrypt 해시, 실패 5회 잠금), 로그인 유지 토큰(DB에는 해시만 저장), 초대 코드 가입, 사용자별 서버 저장
- 앱 시작 시 순서대로 적용되는 SQL 마이그레이션 (`migrations/*.sql`)
- Oracle Cloud VM + systemd + Cloudflare 터널(HTTPS) 배포 및 운영
- ICT 이노베이션 스퀘어 Voice-AI 부트캠프 개인 프로젝트로 36시간 안에 개발·발표하여 **최우수상 수상**

### 🤖 LLM · RAG 학습 (모두의연구소 LLM 5기)
LangChain RAG 파이프라인, RAG 평가 지표, Text-to-SQL 기반 ETF 추천 챗봇, LangGraph 에이전트(Adaptive/Self/CRAG), 10-K 보고서 문서 파싱 RAG를 구현했습니다. (과제 저장소는 비공개)

## 🏆 수상 · 자격

- **수상**: ICT 이노베이션 스퀘어 Voice-AI 부트캠프 개인 프로젝트 최우수상(2026.11), 방송대 컴퓨터과학과 총장배 소프트웨어 경진대회 은상(2023.8)
- **IT**: 정보처리기사(2023.6), SQL개발자(2023.4), ADsP(2025.6)
- **금융**: 재무위험관리사(국내 FRM, 2024.8), 전산회계 1급(2025.2), 파생상품투자상담사 · 펀드투자상담사 · 외환관리사(2011)

## 🍀 My development tools
 - Language: ![Static Badge](https://img.shields.io/badge/Java-007396?style=flat&logo=Java&logoColor=white)
![Static Badge](https://img.shields.io/badge/C-%2300599C?style=flat&logo=C&logoColor=white)
![Static Badge](https://img.shields.io/badge/Python-3776AB?style=flat&logo=Python&logoColor=white)
 - Framework:
![Static Badge](https://img.shields.io/badge/Spring%20Boot-%236DB33F?style=flat&logo=Spring%20Boot&logoColor=white)
![Static Badge](https://img.shields.io/badge/Spring-%236DB33F?style=flat&logo=Spring&logoColor=white)
![Static Badge](https://img.shields.io/badge/Spring%20Security-%236DB33F?style=flat&logo=Spring%20Security&logoColor=white)
![Static Badge](https://img.shields.io/badge/MyBatis-%23000000?style=flat&logoColor=white)
 - Database: 
![Static Badge](https://img.shields.io/badge/PostgreSQL-%234169E1?style=flat&logo=PostgreSQL&logoColor=white)
![Static Badge](https://img.shields.io/badge/MySQL-%234479A1?style=flat&logo=MySQL&logoColor=white)
![Static Badge](https://img.shields.io/badge/Oracle-%23F80000?style=flat&logo=Oracle&logoColor=white)
![Static Badge](https://img.shields.io/badge/Redis-%23DC382D?style=flat&logo=Redis&logoColor=white)
![Static Badge](https://img.shields.io/badge/Apache%20Kafka-%23231F20?style=flat&logo=Apache%20Kafka&logoColor=white)
![Static Badge](https://img.shields.io/badge/Flyway-%23CC0200?style=flat&logo=Flyway&logoColor=white)
 - Infra:
![Static Badge](https://img.shields.io/badge/Docker-%232496ED?style=flat&logo=Docker&logoColor=white)
![Static Badge](https://img.shields.io/badge/Amazon%20AWS-%23232F3E?style=flat&logo=Amazon%20AWS&logoColor=white)
![Static Badge](https://img.shields.io/badge/Amazon%20EC2-%23FF9900?style=flat&logo=Amazon%20EC2&logoColor=white)
![Static Badge](https://img.shields.io/badge/Amazon%20RDS-%23527FFF?style=flat&logo=Amazon%20RDS&logoColor=white)
![Static Badge](https://img.shields.io/badge/Amazon%20S3-%23569A31?style=flat&logo=Amazon%20S3&logoColor=white)
![Static Badge](https://img.shields.io/badge/GitHub%20Actions-%232088FF?style=flat&logo=GitHub%20Actions&logoColor=white)
![Static Badge](https://img.shields.io/badge/Apache%20Tomcat-%23F8DC75?style=flat&logo=Apache%20Tomcat&logoColor=black)
![Static Badge](https://img.shields.io/badge/Nginx-%23009639?style=flat&logo=Nginx&logoColor=white)
![Static Badge](https://img.shields.io/badge/Linux-%23FCC624?style=flat&logo=Linux&logoColor=black)
 - Development Environment:
![Static Badge](https://img.shields.io/badge/IntelliJ%20IDEA-%23000000?style=flat&logo=IntelliJ%20IDEA&logoColor=white)
![Static Badge](https://img.shields.io/badge/Eclipse%20IDE-%232C2255?style=flat&logo=Eclipse%20IDE&logoColor=white)
![Static Badge](https://img.shields.io/badge/Gradle-%2302303A?style=flat&logo=Gradle&logoColor=white)
![Static Badge](https://img.shields.io/badge/Maven-%23C71A36?style=flat&logo=Apache%20Maven&logoColor=white)
![Static Badge](https://img.shields.io/badge/Git-%23F05032?style=flat&logo=Git&logoColor=white)
![Static Badge](https://img.shields.io/badge/Subversion-%23809CC9?style=flat&logo=Subversion&logoColor=white)
![Static Badge](https://img.shields.io/badge/GitHub-%23181717?style=flat&logo=GitHub&logoColor=white)
 - Frontend:
![Static Badge](https://img.shields.io/badge/HTML5-%23E34F26?style=flat&logo=HTML5&logoColor=white)
![Static Badge](https://img.shields.io/badge/CSS3-%231572B6?style=flat&logo=CSS3&logoColor=white)
![Static Badge](https://img.shields.io/badge/Bootstrap-%237952B3?style=flat&logo=Bootstrap&logoColor=white)
![Static Badge](https://img.shields.io/badge/JavaScript-%23F7DF1E?style=flat&logo=JavaScript&logoColor=black)
![Static Badge](https://img.shields.io/badge/React-%2361DAFB?style=flat&logo=React&logoColor=black)
![Static Badge](https://img.shields.io/badge/jQuery-%230769AD?style=flat&logo=jQuery&logoColor=white)
![Static Badge](https://img.shields.io/badge/JSP-007396?style=flat&logo=JSP&logoColor=white)

## 📗 Also on GitHub
 - <a href="https://github.com/greenkey20/algorithm" target="_blank">algorithm</a>: 알고리즘 문제 풀이
 - <a href="https://github.com/greenkey20/spring-workspace" target="_blank">spring-workspace</a>: Spring MVC·AJAX 학습 코드

## ✉️ How to reach me
 - Email: greenkey20dev@gmail.com
 - CV: <a href="https://greenkey20.notion.site/eunyoung-kang" target="_blank">Notion page</a>

[![Solved.ac프로필](https://mazassumnida.wtf/api/v2/generate_badge?boj=greenkey20)](https://solved.ac/greenkey20)
