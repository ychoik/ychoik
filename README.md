<!--
Profile design: light blue banner, original technology colors.
Visual tools: Capsule Render, Skill Icons (light), Shields.io.
-->
<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=rounded&amp;color=0:EAF6FF,100:CFE8F8&amp;height=180&amp;text=CHAN%20IK&amp;fontColor=355C7D&amp;fontSize=46&amp;fontAlignY=40&amp;desc=Backend%20Developer&amp;descSize=19&amp;descAlignY=68" width="100%" alt="CHAN IK — Backend Developer" />
</p>

<h2 align="center">안녕하세요, 백엔드 개발자 윤찬익입니다.</h2>

<p align="center">
  <b>실시간 통신의 응답성과 서비스의 안정성을 개선합니다.</b><br>
  Java · Spring Boot를 중심으로 서비스를 개발하며,<br>
  비동기 처리 구조 개선과 로그 기반 장애 분석, API 문서화를 통한 협업을 경험했습니다.
</p>

<p align="center">
  <img src="https://skillicons.dev/icons?i=java,spring,mysql,mongodb,docker,aws&amp;theme=light&amp;perline=6" height="40" alt="Java, Spring, MySQL, MongoDB, Docker, AWS" />
</p>

<p align="center">
  <a href="https://www.notion.so/CHAN-IK-YUN-4b6dedc0d781826281ff81b143747e3b">
    <img src="https://img.shields.io/badge/Portfolio-729DC2?style=for-the-badge&amp;logo=notion&amp;logoColor=white" alt="Notion 포트폴리오" />
  </a>
  <a href="https://github.com/Team-Kohere/Kohere-backend">
    <img src="https://img.shields.io/badge/Kohere-5E9F9A?style=for-the-badge&amp;logo=github&amp;logoColor=white" alt="Kohere 저장소" />
  </a>
</p>

<br>

<table align="center">
  <tr>
    <td align="center" width="33%">
      <img src="https://img.shields.io/badge/PERFORMANCE-729DC2?style=flat-square" alt="성능 개선" /><br><br>
      <b>468.3 → 26.6 ms</b><br>
      <sub>메시지 저장 확인 ACK</sub>
    </td>
    <td align="center" width="34%">
      <img src="https://img.shields.io/badge/RELIABILITY-5E9F9A?style=flat-square" alt="장애 대응" /><br><br>
      <b>Metaspace OOM</b><br>
      <sub>원인 분석 · 설정 보완</sub>
    </td>
    <td align="center" width="33%">
      <img src="https://img.shields.io/badge/RESEARCH-9294BB?style=flat-square" alt="연구 프로젝트" /><br><br>
      <b>72.5 → 97.3%</b><br>
      <sub>MagNavi 프로젝트 측정 정확도</sub>
    </td>
  </tr>
</table>

<br>

## 📌 Projects

### 01. Kohere
**외국인 맞춤형 주거 탐색 플랫폼**

한국에서 집을 구하는 외국인이 조건에 맞는 매물을 찾고,
언어 장벽 없이 실시간으로 소통할 수 있도록 돕는 서비스입니다.

담당: 실시간 채팅 · 자동 번역 · 푸시 알림 · 매물 검색 개선

- **채팅 응답 개선** — WebSocket·STOMP 기반 채팅에서 메시지 저장 확인과 번역 처리를 분리했습니다. 측정된 ACK 응답 시간을 **468.3ms → 26.6ms, 약 94.3% 단축**했습니다.
- **번역 작업 관리** — 번역 작업 상태와 시도 횟수를 DB에 저장하고, 일시적인 오류에 대한 재시도와 작업 복구 흐름을 구성했습니다.
- **장애 원인 분석** — 로그로 번역 중단의 원인을 Metaspace OOM으로 파악하고, 상한을 **160MB → 256MB**로 조정했습니다. OOM 발생 시 JVM 종료와 컨테이너 재시작 설정도 보완했습니다.
- **푸시 알림·협업** — FCM 기기 토큰 등록·갱신·중복 처리를 구현하고, Spring REST Docs 기반 API 명세를 Swagger UI로 공유해 프론트엔드와 협업했습니다.
- **매물 검색 개선** — MongoDB를 활용해 같은 방이 가격·옵션 조건을 모두 충족하도록 검색하고, 해당 방을 기준으로 가격 표시와 정렬을 개선했습니다.

<sub>ACK는 발신자에게 전달하는 메시지 저장 확인 응답입니다.</sub>
<!-- 성능 측정 환경·요청 수·통계 기준을 정리한 문서를 추가해 연결하세요. 아래 PR은 구현 근거입니다. -->

[프로젝트 저장소](https://github.com/Team-Kohere/Kohere-backend)
· [번역 처리 PR](https://github.com/Team-Kohere/Kohere-backend/pull/259)
· [장애 대응 PR](https://github.com/Team-Kohere/Kohere-backend/pull/282)
· [FCM 기기 관리 PR](https://github.com/Team-Kohere/Kohere-backend/pull/302)

<br>

### 02. MagNavi
**자기장 기반 실내 위치 추정 및 내비게이션**

스마트폰에서 수집한 자기장과 이동 데이터를 활용해,
실내에서도 사용자의 위치를 파악하고 길을 안내하는 서비스입니다.

- **서버 개발** — 센서 데이터를 받아 위치 추정 결과를 반환하는 API 및 데이터베이스를 설계했습니다.
- **위치 추정 개선** — 자기장 보정 알고리즘을 적용해 프로젝트 측정 기준 정확도를 **72.5% → 97.3%, 24.8%p 향상**했습니다.
- **인프라 구축** — AWS EC2·RDS 기반 서버 및 데이터베이스 운영 환경을 구축했습니다.

[프로젝트 저장소](https://github.com/ychoik/magnavi-positioning-service)
· [시연 영상](https://www.youtube.com/watch?v=kqR17mF1d1U)
· [관련 논문](https://www.dbpia.co.kr/journal/articleDetail?nodeId=NODE12567180)

<br>

### 03. Paperdot
**영어 원문과 번역문을 문장별로 연결하는 학습 서비스**

영어 PDF의 원문과 번역문을 문장 단위로 나란히 읽으며,
내용을 이해하고 학습할 수 있도록 돕는 문서 리더 서비스입니다.

- **문서 분석** — PDF에서 텍스트를 추출하고 문장 단위로 분리했습니다.
- **번역 매칭** — 문장별 번역 결과를 원문과 1:1로 연결해 저장·조회하는 기능을 구현했습니다.
- **사용자 인증** — OAuth2 로그인 및 JWT 기반 인증을 구현했습니다.

[프로젝트 저장소](https://github.com/ychoik/be-paper-reader_myself)

---

## 🛠 Tech Stack

### Backend & Language

<p>
  <img src="https://img.shields.io/badge/Java-ED8B00?style=flat-square&amp;logo=openjdk&amp;logoColor=white" alt="Java" />
  <img src="https://img.shields.io/badge/Spring%20Boot-6DB33F?style=flat-square&amp;logo=springboot&amp;logoColor=white" alt="Spring Boot" />
  <img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&amp;logo=python&amp;logoColor=white" alt="Python" />
  <img src="https://img.shields.io/badge/FastAPI-009688?style=flat-square&amp;logo=fastapi&amp;logoColor=white" alt="FastAPI" />
</p>

REST API와 비동기 처리, 센서 데이터 처리 및 위치 추정 API 개발에 활용했습니다.

### Database

<p>
  <img src="https://img.shields.io/badge/MySQL-4479A1?style=flat-square&amp;logo=mysql&amp;logoColor=white" alt="MySQL" />
  <img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&amp;logo=postgresql&amp;logoColor=white" alt="PostgreSQL" />
  <img src="https://img.shields.io/badge/MongoDB-47A248?style=flat-square&amp;logo=mongodb&amp;logoColor=white" alt="MongoDB" />
</p>

### Real-time & Notification

<p>
  <img src="https://img.shields.io/badge/FCM-FFCA28?style=flat-square&amp;logo=firebase&amp;logoColor=333333" alt="FCM" />
</p>

WebSocket · STOMP 기반 실시간 채팅과 메시지 저장 확인 ACK, FCM 푸시 알림을 구현했습니다.

### Infrastructure & Delivery

<p>
  <img src="https://img.shields.io/badge/AWS-FF9900?style=flat-square" alt="AWS" />
  <img src="https://img.shields.io/badge/Docker-2496ED?style=flat-square&amp;logo=docker&amp;logoColor=white" alt="Docker" />
  <img src="https://img.shields.io/badge/GitHub%20Actions-2088FF?style=flat-square&amp;logo=githubactions&amp;logoColor=white" alt="GitHub Actions" />
</p>

서버 환경 구성, 컨테이너 배포와 배포 자동화에 활용했습니다.

### Test & Documentation

<p>
  <img src="https://img.shields.io/badge/JUnit%205-25A162?style=flat-square&amp;logo=junit5&amp;logoColor=white" alt="JUnit 5" />
  <img src="https://img.shields.io/badge/Spring%20REST%20Docs-6DB33F?style=flat-square" alt="Spring REST Docs" />
  <img src="https://img.shields.io/badge/Swagger%20UI-85EA2D?style=flat-square&amp;logo=swagger&amp;logoColor=173647" alt="Swagger UI" />
</p>

API 동작을 검증하고, API 명세와 연동 가이드를 공유하며 협업했습니다.

### Collaboration

<p>
  <img src="https://img.shields.io/badge/Git-F05032?style=flat-square&amp;logo=git&amp;logoColor=white" alt="Git" />
  <img src="https://img.shields.io/badge/Slack-4A154B?style=flat-square&amp;logo=slack&amp;logoColor=white" alt="Slack" />
</p>

---

## 🏆 Awards & Publications

| 시기 | 수상·논문 |
| :--- | :--- |
| 2025.12.02 | MIDAS GROUP 최종발표회 **대상** |
| 2025.10.21 | 한국통신학회(KICS) 추계학술대회 **논문 게재** · [논문 보기](https://www.dbpia.co.kr/journal/articleDetail?nodeId=NODE12567180) |
| 2025.09.27 | 2025년 캡스톤디자인 경진대회 **최우수상** |
| 2025.09.09 | 제1회 MIDAS CDP 경진대회 **최우수상** |

## 🌱 Education & Activities

| 기간 | 교육·활동 |
| :--- | :--- |
| 2026.07 ~ 현재 | 삼성청년SW·AI아카데미 **SSAFY 16기** |
| 2026.05 ~ 2026.08 | IT 사이드 프로젝트 프로그램 **SWYP 앱 5기 수료** |
| — | IT 사이드 프로젝트 프로그램 **SWYP 웹 12기 수료** |
| 2024 ~ 2025 | 교내 IT 개발 동아리 **회장** |
| 2023.09 | 디지털 금융 인재 양성과정 수료 · 메가존클라우드 아이티 평생교육원 · AWS 및 클라우드 교육 |

<!-- SWYP 웹 12기 활동 기간은 확인 후 추가합니다. -->

---

## 🔗 Contact

[Notion 포트폴리오](https://www.notion.so/CHAN-IK-YUN-4b6dedc0d781826281ff81b143747e3b)

<!--
Optional contact — intentionally unpublished:
mailto:yooni06151236@gmail.com
-->
