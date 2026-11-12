# GENIE.AI · Zindi · 도시특화 시스템 | 핵심 Q&A와 사전 검증

**기준:** 2026-11-12 / IEEE 및 GENIE 공식 공개 문서 확인. **상태:** 설계·테스트 계획이며, GENIE를 실제 설치·구동한 것은 아님.

## 핵심 결론

**제안 대상은 '도시 전용 언어모델'이 아니라 '도시 업무를 처리하는 AI 서비스'다.** 기존 오픈소스 언어모델 + 근거 검색 + GIS/수치 계산 + 사람의 검수 + 도시용 UI를 결합한다.

## Q&A

### Q1. 1차 단계에서 무엇을 제출하나?
IEEE Funding Portal에는 **선정 도시 1곳의 문제를 해결하는 기술·운영·검증 계획**을 제출한다. Zindi에서는 **제한된 소형 모델과 허용 도구로 자료 기반 문제에 답하고 근거를 남기는 재현 가능한 기술시험**을 수행한다. 두 작업은 연결되지만 **동일한 제품을 개발해 제출하는 것은 아니다.**

### Q2. GENIE는 언제 필요한가? 최종 우승 후 처음 쓰나?
아니다. 공식 현재 모집 페이지는 팀의 GENIE 사용을 **필수**로 안내하며, **1차 제안서에는 통합 계획만 설명하면 되고 Zindi 기술시험은 GENIE 사용 대상이 아니라고 명시**한다. 제안서 단계에서 GENIE 아키텍처와 통합 위험을 살피고, 준결선에서 도시 담당자와 요구사항을 재정의하고, 결선 단계에서 시제품 구현, 최종 선정 시 현장 실증으로 이어진다. 실제 구현 단계·조건은 심사/지원 계약에 따라 확인한다.

### Q3. GENIE는 AI 모델인가?
아니다. GENIE는 공공 부문을 위한 **오픈소스 AI 서비스 프레임워크**다. 로그인/권한(Keycloak), 자료 저장·색인, 검색 기반 답변(RAG), 모델 연결(vLLM/OPEA 구성), 웹 UI와 운영·관측 기능을 묶는다. **모델 자체와 도시 GIS·에너지 계산 엔진을 자동으로 제공하는 것은 아니다.**

### Q4. 도시 전용 모델을 새로 학습해야 하나?
필수조건으로 확인되지 않았다. 공개 오픈소스 모델에 도시 자료를 검색 연결하고 전문 분석 도구를 결합하는 방식이 합리적이다. 필요하면 검증 후 후속 학습을 고려하되, 초기 제안에서 무조건 미세조정을 약속하지 않는다.

### Q5. Zindi의 3B 제한이 도시 시제품에도 적용되나?
**구분해야 한다.** 3B 이하 모델 제약은 Zindi 기술평가 규정의 조건이다. 이후 도시 서비스를 똑같이 3B로 제한한다는 요구는 현재 확인되지 않았다. GENIE의 기본 모델 규모·GPU 자원·데이터 주권 요건은 별도 검토한다.

### Q6. ChatGPT가 문제를 풀면 시험이 끝나나?
설계·분석·검증을 돕고 샘플 문제를 독립적으로 풀어볼 수는 있다. 그러나 공식 Zindi 답안은 **주어진 모델/호출/데이터 제한에 맞춰 실행·재현 가능한 코드와 출처**로 생성해야 한다. ChatGPT의 응답을 규정 적합성 검증 없이 공식 결과라고 간주하지 않는다.

### Q7. AIRTECT는 어떻게 연결하나?
- **F.AIR:** 문서 근거·교차검증·보고서 작성의 참고 기술
- **V.AIR:** 지도·대상지·GIS 시각화/공간분석의 참고 기술
- **AIPM:** 프로젝트 정형 데이터·상태 관리 패턴
- **AIRender:** 필요성이 입증된 경우에만 시각화 지원
- **GENIE:** 출품용 도시 AI 서비스의 공통 기반으로 통합
- **별도 전문 API:** 스코페의 수목·행정문서 좌표 매칭 또는 리브네의 비용·절감량 계산

기존 AIRTECT 제품을 통째로 이식하거나 F.AIR/ADK를 통째로 폐기하는 것으로 가정하지 않는다. 실증 요건·라이선스·로그인/권한·운영 부담을 기준으로 필요한 기능만 이관/재작성한다.

### Q8. 예를 들어 스코페 시제품은 어떤 모습인가?
행정 담당자가 변경 문서(PDF/도면)를 입력 → 자료 추출·근거 출처 표시 → GIS의 기존 수목/녹지 정보와 대조 → 변경 후보·오류/불확실성 표시 → 담당자 승인 → 확인된 변경만 시스템에 반영. GENIE가 검색과 AI 서비스를 제공하더라도 **좌표 정합·면적 계산·수목 대장 갱신·검수 UI는 직접 개발/연결**해야 한다.

### Q9. 선정 이후에만 GENIE를 테스트해도 되나?
권하지 않는다. 현재는 **GENIE 기본 설치, 문서 검색, 인증, 외부 전문 API 연결 가능성**만 검증하면 충분하다. 제안서에서 구현 가능성을 뒷받침할 증거가 된다. 단, 아직 실증 도시 데이터가 없으므로 별도 공개/더미 데이터로 평가해야 한다.

## 최소 사전 검증 · 3단계

| 단계 | 환경 | 실행 범위 | 통과 기준 |
|---|---|---|---|
| **A. 구조 검토** | 문서/코드 읽기 | GENIE 서비스 경계·API·권한·라이선스·요구 자원 파악 | 필요한 통합 포인트·제약·비용을 문서화 |
| **B. CPU 스모크 테스트** | 별도 개발 머신/격리된 VM, Docker Compose, 8vCPU·16GB RAM 권장 | 코어 UI, Keycloak 로그인, API 상태 확인 | `/api/health` 정상, 관리자 로그인, 서비스 의존성 healthy |
| **C. AI 및 도시 전문기능 POC** | 모델용 GPU 또는 격리된 원격 모델 노드 | 공식 OPEA + GPU 모델 구성, 테스트 PDF 1건 근거 답변, 도시 API 모의 호출 | 근거 문서가 추적되고 계산결과가 재현되며 미확인 자료를 사실로 답하지 않음 |

> **한계:** `docker compose up -d`만 실행한 CPU-only core는 관리자/웹/API를 확인할 수 있지만 **LLM 답변은 작동하지 않는다.** 공식 문서에 따르면 RAG 답변까지는 `opea` 및 모델 구동 환경이 추가로 필요하다.

### 설치 예시 (별도의 테스트 PC/VM · 아직 실행하지 않음)

실제 비밀번호·이메일·클라이언트 비밀값은 `.env`에 별도로 설정하고 **절대 Git에 저장하지 않는다.**

```bash
git clone https://opensource.unicc.org/un/itu/genie-ai.git
cd genie-ai
cp env .env
# .env: ARANGO_PASSWORD, TRANSLATION_CACHE_PASSWORD,
# POSTGRES_PASSWORD, KONG_DB_PASSWORD, KEYCLOAK_DB_PASSWORD,
# KEYCLOAK_ADMIN_PASSWORD, GENIE_ADMIN_PASSWORD,
# KEYCLOAK_CLIENT_SECRET 등 공식 필수 변수 확인
# 로컬 테스트용 로그인 검증메일을 설정하지 않는 경우:
# KEYCLOAK_VERIFY_EMAIL=false (외부 노출 서버에 그대로 사용하지 않기)

docker compose config >/dev/null
docker compose up -d
docker compose ps
curl -sk https://localhost/api/health
```

기대치: `/api/health`가 `status: ok`에 해당하는 JSON을 반환하고, 자체서명 인증서를 허용한 `https://localhost`에서 Keycloak 로그인에 성공한다. AI 채팅은 별도 프로필에서 검증한다.

GPU가 준비되고 비용이 승인됐을 때만 공식 권장 구성을 확인하여 시작한다.

```bash
docker compose --profile opea --profile gpu-models up -d
# 이 단계는 Hugging Face 모델 다운로드, GPU 및 추가 리소스 필요
```

**주의:** 테스트 서버를 인터넷에 바로 공개하지 않는다. 기존 AIR 운영 서버/DB/Supabase에 붙이지 않는다. 외부 서비스 키·원본 도시 문서가 없는 독립 환경에서 시작한다. GPU 프로필 가동은 요금 발생 가능.

## 최소 POC 시나리오

- 자료: 공개된 녹지/에너지 관련 문서 1건 또는 만든 샘플 1건
- 질문: '이 문서에서 바뀐 항목은 무엇이며, 어느 문장이 근거인가?'
- 별도 Python API: `GET /mock/site-record`로 더미 GIS/건물 레코드 1건
- 점검: **문서 출처**, **계산/API 결과와 언어모델 추측의 구분**, **검수/승인 단계**, **실행 로그**
- 산출물: 1장 구조도 + 작동 기록/스크린샷 + 예상 운영비 + 미해결 위험 목록

## 공식 근거

- [IEEE 모집안내 · GENIE 사용 및 Zindi 예외](https://ieeeht.org/get-involved/funding-opportunities/genai-for-good/)
- [GENIE 소개 / 시스템 경계](https://genie-ai-7e342b.opensource.unicc.org/docs/get-started/welcome/)
- [GENIE 설치 가이드](https://genie-ai-7e342b.opensource.unicc.org/docs/deploy/install-guide/)
- [GENIE 로컬 배포 퀵스타트](https://genie-ai-7e342b.opensource.unicc.org/docs/get-started/quickstart-deployer/)
- [GENIE Docker Compose](https://genie-ai-7e342b.opensource.unicc.org/docs/deploy/docker-compose-setup/)
- [GENIE 개발 확장 가이드](https://genie-ai-7e342b.opensource.unicc.org/docs/get-started/quickstart-developer/)

**검증되지 않은 사항:** GENIE 실제 로컬 부팅, 사용 가능한 GPU 사양·비용, 최신 브랜치의 API 호환성, GIS 전문 도구 연동은 아직 테스트 전.
