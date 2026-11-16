# Hi, I am Eunyoung 👋

금융 SI/솔루션 분야에서 일하는 **Java · Spring 백엔드 개발자**입니다.<br>
문제를 풀고 데이터를 다루는 일을 좋아하고, 직접 만들고 배포하며 배웁니다.

## 💼 What I do

- **금융 SI/솔루션 백엔드 개발**
  - Java · Spring Boot · PostgreSQL 기반 백엔드 개발 (2년)
  - Proframe(C) 기반 고객사 계정계 개발, Oracle (1년)
- 회사 밖에서는 개인 프로젝트로 인증, DB 마이그레이션, 컨테이너, 배포까지 혼자 설계하고 운영해 봅니다.

## 🚀 Projects

### 🪐 [Inner Orbit](https://github.com/greenkey20/inner-orbit): 감정·인사이트 로그 서비스 (백엔드 중심 개인 프로젝트)
`Java 21` `Spring Boot 3.5` `Spring Security` `JPA` `PostgreSQL` `Flyway` `Redis` `Docker Compose` `React`

개발자의 일상·감각·통찰을 구조화해서 기록하고, AI로 패턴을 분석하는 멀티 유저 웹 서비스입니다.
- **JWT 인증/인가**: Spring Security + jjwt, BCrypt 해시, 사용자별 데이터 완전 격리(users 테이블 + FK)
- **DB 마이그레이션 운영 규칙**: Flyway로 스키마 변화를 관리. 커밋된 migration은 수정·삭제하지 않고 새 버전으로 고치는 원칙을 세워 운영 DB와 어긋나지 않게 관리
- **PostgreSQL JSONB**로 모드별(Daily/Sensory/Insight) 데이터 스키마를 분리하고 V5/V6 마이그레이션으로 이전
- **Redis**로 AI 질문 이력을 TTL 30일로 관리해 반복 방지, **`@Scheduled`** 주간 리포트 자동 생성
- **Spring AI**로 OpenAI를 연동하고, 저장 전 분석은 Stateless API로 분리
- Docker Compose(PostgreSQL · Redis · Nginx)로 개발·운영 환경 구성

### 🎵 [song-lingo](https://github.com/greenkey20/song-lingo): 외국어 문장 발음·받아쓰기 연습 서비스 (기획부터 배포까지 1인 개발)
`Python` `Streamlit` `faster-whisper` `PostgreSQL` `Oracle Cloud` `Cloudflare Tunnel`

듣고 따라읽거나 받아쓰면 STT로 인식해 오류율(WER/CER)과 틀린 부분을 알려주는 음성 학습 앱입니다. **https://songlingo.kr** 에서 실제로 운영 중입니다.
- 로그인(scrypt 해시, 실패 5회 잠금), 로그인 유지 토큰(DB에는 해시만 저장), 초대 코드 가입, 사용자별 서버 저장
- 앱 시작 시 순서대로 적용되는 SQL 마이그레이션 (`migrations/*.sql`)
- Oracle Cloud VM + systemd + Cloudflare 터널(HTTPS) 배포 및 운영
- 부트캠프(ICT 혁신 스퀘어 Voice-AI) 개인 프로젝트로 36시간 안에 개발해 발표

### 🤖 LLM · RAG 학습 (모두의연구소 LLM 5기)
LangChain RAG 파이프라인, RAG 평가 지표, Text-to-SQL 기반 ETF 추천 챗봇, LangGraph 에이전트(Adaptive/Self/CRAG), 10-K 보고서 문서 파싱 RAG를 구현했습니다. (과제 저장소는 비공개)

## 🍀 My development tools
 - Language: ![Static Badge](https://img.shields.io/badge/Java-007396?style=flat&logo=Java&logoColor=white)
![Static Badge](https://img.shields.io/badge/Python-3776AB?style=flat&logo=Python&logoColor=white)
 - Framework:
![Static Badge](https://img.shields.io/badge/Spring%20Boot-%236DB33F?style=flat&logo=Spring%20Boot&logoColor=white)
![Static Badge](https://img.shields.io/badge/Spring-%236DB33F?style=flat&logo=Spring&logoColor=white)
![Static Badge](https://img.shields.io/badge/Spring%20Security-%236DB33F?style=flat&logo=Spring%20Security&logoColor=white)
 - Database: 
![Static Badge](https://img.shields.io/badge/PostgreSQL-%234169E1?style=flat&logo=PostgreSQL&logoColor=white)
![Static Badge](https://img.shields.io/badge/MySQL-%234479A1?style=flat&logo=MySQL&logoColor=white)
![Static Badge](https://img.shields.io/badge/Oracle-%23F80000?style=flat&logo=Oracle&logoColor=white)
![Static Badge](https://img.shields.io/badge/Redis-%23DC382D?style=flat&logo=Redis&logoColor=white)
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
 - <a href="https://github.com/greenkey20/knou-key-project" target="_blank">Alloc</a>: 테스트 및 리팩토링
 - <a href="https://github.com/greenkey20/algorithm" target="_blank">algorithm</a>: 알고리즘 문제 풀이

## ✉️ How to reach me
 - Email: greenkey20dev@gmail.com
 - CV: <a href="https://greenkey20.notion.site/eunyoung-kang" target="_blank">Notion page</a>
 - Blog: <a href="https://greenkey20dev.tistory.com" target="_blank">greenkey20dev.tistory.com</a>

[![Solved.ac프로필](http://mazassumnida.wtf/api/v2/generate_badge?boj=greenkey20)](https://solved.ac/greenkey20)
