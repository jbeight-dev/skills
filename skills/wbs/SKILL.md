# Skill.md
# Data Platform 기능 개발 프로젝트 WBS 작성 가이드

---

# 1. 목적

본 문서는 데이터 플랫폼 신규 기능 개발 프로젝트 수행 시
프로젝트 리더가 일관된 방식으로 WBS(Work Breakdown Structure)를 작성하기 위한 기준을 정의한다.

목표:
- 일정 산정 가능
- 역할 분리 명확화
- 누락 없는 작업 정의
- 진행률 관리 가능
- 분석/설계/개발/테스트 단계 추적 가능

---

# 2. 기본 원칙

## 2.1 기능 중심으로 작성한다

좋지 않은 예:
- 화면 개발
- API 개발

좋은 예:
- Data Catalog 검색 API 개발
- 자동완성 Suggest API 개발
- 검색 결과 필터 UI 개발

---

## 2.2 산출물이 보이도록 작성한다

모든 Task는 결과물이 명확해야 한다.

예:
- 요구사항 정의서 작성
- API 명세 작성
- ERD 작성
- OpenSearch Index 생성
- 검색 UI 구현

---

## 2.3 3~5일 이내 단위로 분할한다

하나의 Task는 너무 크지 않도록 작성한다.

좋지 않은 예:
- AI Assistant 개발

좋은 예:
- Prompt 구조 설계
- Retriever 설계
- LangChain Flow 구현
- FAQ RAG 연동
- 대화 이력 저장 구현

---

## 2.4 단계 기반으로 분리한다

권장 단계:
1. 분석
2. 설계
3. 개발
4. 테스트
5. 배포
6. 안정화

---

# 3. 데이터 플랫폼 프로젝트 권장 WBS 구조

## Level 1
프로젝트

## Level 2
기능 영역

예:
- Data Catalog
- AI Assistant
- Search
- Glossary
- Governance

## Level 3
구현 기능

예:
- 자동완성
- 통합검색
- 자연어 탐색
- Text-to-SQL
- RAG Chat

## Level 4
작업 단계

예:
- 요구사항 분석
- 화면 설계
- API 설계
- Backend 개발
- Frontend 개발
- 테스트

---

# 4. 권장 Task 유형

## 4.1 분석 단계

### 목적
무엇을 만들지 정의

### 주요 Task
- 요구사항 분석
- 사용자 시나리오 작성
- AS-IS 분석
- TO-BE 정의
- 데이터 흐름 분석
- 메타데이터 구조 분석
- API 인터페이스 분석
- 사용자 검색 패턴 분석

---

## 4.2 설계 단계

### 목적
어떻게 만들지 정의

### 주요 Task
- 아키텍처 설계
- 화면 Wireframe 작성
- API 명세 설계
- ERD 설계
- OpenSearch Index 설계
- LangChain 구조 설계
- RAG 구조 설계
- Prompt 설계
- 권한 구조 설계
- 캐시 전략 설계

---

## 4.3 개발 단계

### Backend
- API 개발
- Batch 개발
- Metadata 수집 개발
- OpenSearch 연동
- VectorDB 연동
- AI Model 연동

### Frontend
- 검색 UI 개발
- 자동완성 UI 개발
- Chat UI 개발
- 필터 UI 개발
- 상세 화면 개발

### AI
- Retriever 구현
- Prompt 구현
- Chain 구현
- Agent Flow 구현
- Embedding Pipeline 구현

---

## 4.4 테스트 단계

### 주요 Task
- 단위 테스트
- 통합 테스트
- 검색 품질 테스트
- Prompt 품질 테스트
- 성능 테스트
- 사용자 시나리오 테스트
- 장애 테스트

---

## 4.5 배포 단계

### 주요 Task
- 운영 배포
- Helm 배포
- Config 적용
- Secret 설정
- 모니터링 설정
- 로그 수집 설정

---

# 5. 데이터 플랫폼 특화 WBS 작성 팁

## 5.1 검색 기능은 품질 개선 Task를 반드시 포함한다

예:
- 검색 Ranking 개선
- 동의어 사전 구축
- 검색 로그 분석
- 추천 검색어 구축
- 검색 정확도 측정

---

## 5.2 AI 기능은 Prompt/RAG Task를 반드시 분리한다

좋지 않은 예:
- AI Assistant 개발

좋은 예:
- FAQ 데이터 수집
- Chunk 전략 설계
- Embedding 생성
- Retriever 설계
- Prompt 설계
- 답변 품질 평가

---

## 5.3 Metadata 프로젝트는 구조 분석을 반드시 포함한다

예:
- Catalog 구조 분석
- Table/Column Metadata 분석
- Description 품질 분석
- Tag 체계 분석
- Lineage 구조 분석

---

# 6. 권장 WBS 컬럼

| 컬럼 | 설명 |
|---|---|
| ID | WBS ID |
| Phase | 분석/설계/개발/테스트 |
| Task | 작업명 |
| Detail | 상세 설명 |
| Owner | 담당자 |
| Duration | 예상 기간 |
| Dependency | 선행 작업 |
| Deliverable | 산출물 |
| Status | 진행 상태 |

---

# 7. 좋은 WBS 예시

| ID | Phase | Task | Deliverable |
|---|---|---|---|
| 1.1 | 분석 | 검색 요구사항 정의 | 요구사항 정의서 |
| 1.2 | 분석 | 사용자 검색 시나리오 작성 | 사용자 시나리오 |
| 1.3 | 설계 | 자동완성 구조 설계 | 설계서 |
| 1.4 | 설계 | OpenSearch Index 설계 | Index 정의서 |
| 1.5 | 개발 | Suggest API 개발 | Backend API |
| 1.6 | 개발 | 자동완성 UI 개발 | Frontend UI |
| 1.7 | 테스트 | 검색 품질 테스트 | 테스트 결과서 |

---

# 8. 나쁜 WBS 예시

| 문제 유형 | 예시 |
|---|---|
| 너무 큼 | AI 시스템 개발 |
| 결과물 불명확 | 기능 수정 |
| 일정 산정 불가 | 검색 개선 |
| 역할 불명확 | 플랫폼 작업 |
| 단계 없음 | 개발만 존재 |

---

# 9. 프로젝트 리더 체크리스트

## 분석
- 사용자 시나리오가 있는가?
- 현재 문제점이 정의되었는가?
- 범위가 명확한가?

## 설계
- API/ERD/UI가 정의되었는가?
- 운영 구조가 고려되었는가?
- 권한 구조가 정의되었는가?

## 개발
- Backend/Frontend 분리가 되었는가?
- AI Flow가 분리되었는가?
- 공통 모듈이 정의되었는가?

## 테스트
- 품질 측정 기준이 있는가?
- 성능 기준이 있는가?
- 사용자 검증 계획이 있는가?

---

# 10. 데이터 플랫폼 프로젝트 추천 Phase 예시

1. 요구사항 분석
2. 사용자 시나리오 정의
3. Metadata 구조 분석
4. 검색 구조 설계
5. AI/RAG 구조 설계
6. API 설계
7. Backend 개발
8. Frontend 개발
9. AI Flow 개발
10. 통합 테스트
11. 성능 테스트
12. 운영 배포
13. 안정화

---

# 11. 핵심 원칙 요약

- 기능 중심으로 작성
- 산출물이 보여야 함
- 3~5일 단위로 분할
- 분석/설계/개발/테스트 구분
- AI 기능은 RAG/Prompt/Retriever 분리
- 검색 기능은 품질 개선 포함
- Metadata 구조 분석을 반드시 수행