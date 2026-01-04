## 🧱 My Stacks

### 🌐 Languages
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-323330.svg?style=for-the-badge&logo=javascript&logoColor=F7DF1E)
![Java](https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)

### 🧩 Frameworks / Libraries
![Spring Boot](https://img.shields.io/badge/Spring%20Boot-6DB33F?style=for-the-badge&logo=springboot&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white)
![React](https://img.shields.io/badge/React-20232a.svg?style=for-the-badge&logo=react&logoColor=61DAFB)
![Next.js](https://img.shields.io/badge/Next.js-000000?style=for-the-badge&logo=next.js&logoColor=white)

### 🗄️ Databases
![MariaDB](https://img.shields.io/badge/MariaDB-003545?style=for-the-badge&logo=mariadb&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-4479A1.svg?style=for-the-badge&logo=mysql&logoColor=white)
![Neo4j](https://img.shields.io/badge/Neo4j-018BFF?style=for-the-badge&logo=neo4j&logoColor=white)

### ☁️ Infra / DevOps
![AWS](https://img.shields.io/badge/AWS-232F3E?style=for-the-badge&logo=amazonaws&logoColor=white)
![Nginx](https://img.shields.io/badge/Nginx-009639?style=for-the-badge&logo=nginx&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub%20Actions-2671E5.svg?style=for-the-badge&logo=githubactions&logoColor=white)

### 🛠️ Tools
![Git](https://img.shields.io/badge/Git-F05033.svg?style=for-the-badge&logo=git&logoColor=white)
![Postman](https://img.shields.io/badge/Postman-FF6C37?style=for-the-badge&logo=postman&logoColor=white)
![Swagger](https://img.shields.io/badge/Swagger-85EA2D?style=for-the-badge&logo=swagger&logoColor=black)


## 🚀 Projects

### 1) HaksaMate — 대학생 통합 플랫폼 (시간표/학사일정/커뮤니티/마켓/실시간 소통)
- Role: Backend 중심 개발 (실시간 기능, 지도/HTTPS, 커뮤니티 기능 구현)
- Stack: Supabase(Auth/DB), PostgreSQL, WebSocket, Next.js/React
- Key Points
  - 시간표 데이터 확장(과목/요일/색상/메모 등)에 대응하기 위해 저장 구조를 확장 가능하게 설계(JSONB 기반 등)
  - 실시간 기능은 단순 Realtime 기능으로 끝내지 않고, 서비스 요구(메시징/상태 동기화)에 맞게 WebSocket 기반 흐름으로 구현
  - 지도 외부 API 사용을 위해 HTTPS 환경을 구성(보안 정책 대응)하고 배포 환경까지 정리
- Links: Repo( ) · Demo( ) · Docs( )

---

### 2) DicomViewer — 웹 기반 DICOM 뷰어(대용량/다양한 포맷 대응)
- Role: Backend/Infra (전송 흐름 설계, 인증, 멀티 DB 운영)
- Stack: Java, Spring Boot, JWT, Redis, Oracle + MariaDB, Nginx/AWS
- Key Points
  - 대용량 파일에서 “한 번에 전송” 방식의 한계를 겪고, 전송 단위/실패 복구 흐름을 먼저 잡는 방향으로 정리
  - Transfer Syntax 등 입력 특성 차이로 발생하는 실패 케이스를 분류하고, 지원 범위/예외 처리 기준을 서버-클라이언트 흐름으로 고정
  - 인증(JWT/Redis)과 멀티 데이터소스(Oracle/MariaDB) 운영 구성요소까지 함께 다루며 서비스 형태로 유지 가능한 구조를 정리
- Links: Repo( ) · Demo( ) · Docs( )

---

### 3) StockPredictor — 온톨로지 기반 주식 분석/의사결정 보조(실패→피벗)
- Role: Data Pipeline / Ontology / API
- Stack: Python, Pandas, Neo4j(Cypher), TensorFlow, FastAPI, Next.js, Playwright/BS4
- Status: 예측 서비스 목표는 성능 미달로 실패 → KRX400 상대 점수 랭킹 어시스턴트로 전환
- Key Points
  - 종목-시계열-날짜를 기준 축으로 News/Event/Sentiment를 관계로 연결하는 온톨로지 구조로 적재(단순 병합이 아니라 관계 질의 가능)
  - LSTM을 직접 구현해 예측을 시도했으나 성능 목표 미달 + 평가 지표/검증 설계 미숙으로 개선이 누적되지 않음
  - 수집 데이터 활용이 가능한 LSR-IGRU로 전환 후 KRX400 재학습, 예측 대신 “상대 점수 기반 랭킹”으로 매수/매도 판단 보조 방향으로 피벗(FastAPI로 랭킹/점수 조회 API 제공)
- Links: Repo( ) · API( ) · Demo( )
