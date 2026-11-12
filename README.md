# IEEE GenAI for Good Challenge — Cities Edition

IEEE Humanitarian Technologies × UNDP의 **GenAI for Good Challenge: Cities Edition (2026–2027)** 참가 검토를 위한 공개 리서치·킥오프 저장소입니다.

> **상태 (2026-11-12): 조사 및 참가 검토 중.** IEEE 지원서 제출·GENIE 설치·서비스 구현은 아직 수행하지 않았습니다. 기술평가 파일 일부는 대화 내 수령·검토했지만 공식 답안 제출 여부는 확인되지 않았습니다. 이 저장소는 IEEE/UNDP의 공식 저장소가 아닙니다.

## 킥오프 발표자료

- **[발표자료 바로 보기 — GitHub Pages](https://kalmsong.github.io/IEEE/)**: 항상 현재 공개한 최신 킥오프 발표자료를 여는 고정 주소입니다. GitHub Pages `main` 브랜치 `/ (root)` 설정이 필요합니다.

- **[v1 — 확정 백업](presentations/GenAI_for_Good_Kickoff_v1.html)**: v0.2와 v0.3을 병합했던 원본 27장. 내용·구조를 수정하지 않고 보존.
- **[v1.1 — 편집 작업본](presentations/GenAI_for_Good_Kickoff_v1.1.html)**: 기존 27장 유지 + 근거 기반 2장 추가. 순서 재배치, 장수 및 내비게이션 개선, 비공개 Zindi 데이터에 대한 표현 정정.
- [변경 이력](presentations/CHANGELOG.md)

최신 발표자료는 저장소 루트 `index.html`에 별도 게시하며, 버전이 확정되면 해당 HTML을 `presentations/`에 보관합니다. HTML 파일은 브라우저에서 열어 한 장씩 넘기는 형식입니다. 키보드 방향키, 하단 이전·다음, 전체 목차를 지원합니다.

## 연구 및 의사결정 자료

| 자료 | 설명 |
|---|---|
| [공모전 개요](docs/PROGRAM_BRIEF.md) | 목적, 제출물, 지원·심사 과정, 일정 |
| [도시 과제 분석](docs/CITY_USE_CASES.md) | 스코페·리브네의 최소 필수기능, 데이터 제공 상태, 개발 위험 |
| [Zindi 기술시험](docs/ZINDI_ASSESSMENT.md) | 제공 파일 목록, 모델·도구 제한, 평가 및 코드 재현성 |
| [GENIE와 시스템 설계](docs/GENIE_ARCHITECTURE.md) | GENIE·언어모델·ADK·도시 전문도구의 역할 분리 |\n| **[GENIE 핵심 Q&A·사전 테스트](docs/GENIE_QA_AND_TEST_PLAN.md)** | Zindi와 GENIE의 시점·역할 구분, 도시특화 AI 시스템, 실제 테스트 방법 |
| [근거 및 출처](docs/SOURCE_REGISTER.md) | 공식 URL, 확인 수준, 조사일 |
| [결정 및 다음 단계](docs/DECISIONS.md) | 확정사항·미결사항·우선 확인 사항 |
| [공개 저장소 운영 원칙](docs/PUBLIC_REPO_POLICY.md) | 비공개 코드·도시 데이터·시험 파일 관리 원칙 |

## 특히 구분해야 할 세 가지

1. **도시 과제**: 스코페(녹지대장) 또는 리브네(에너지 개선 컨설팅) 등 도시 1곳의 실제 업무 문제 해결.
2. **1차 지원**: IEEE 제안서 + Zindi 공통 기술시험. 도시용 웹서비스의 완성은 첫 접수 시 필수 아님.
3. **GENIE.AI**: 도시용 AI의 공통 오픈소스 기반. IEEE 현행 모집페이지 기준 활용 **필수**로 안내. 1차 제안서는 적용 계획, Zindi 시험에서는 사용 요구 없음. 아직 로컬 실설치 전.

## 공식 자료

- [IEEE 공식 안내](https://ieeeht.org/get-involved/funding-opportunities/genai-for-good/)
- [Skopje 공식 과제](https://ieeeht.org/wp-content/uploads/2026/11/GAI4GC-Cities-Edition-Use-Case-Green-Infrastructure-AI-Assistant-Skopje-North-Macedonia.pdf)
- [Rivne 공식 과제](https://ieeeht.org/wp-content/uploads/2026/11/GAI4GC-Cities-Edition-Use-Case-Energy-Advisory-AI-Assistant-Rivne-Ukraine.pdf)
- [Zindi 기술시험](https://zindi.world/competitions/GenAI-for-Good-Challenge)
- [Zindi 데이터 안내](https://zindi.world/competitions/GenAI-for-Good-Challenge/data)
- [GENIE 공식 문서](https://genie-ai-7e342b.opensource.unicc.org/docs/get-started/welcome/)

## 권리 및 데이터

공모전 공식 PDF·Zindi 원천자료는 **원본을 복제하지 않고 링크와 독자적인 조사 메모**로 관리합니다. Zindi 자료에는 원천별 저작권·라이선스와 Train/Test 분리 규정이 적용됩니다. AIRTECT 운영 코드, 비공개 DB, 키·토큰, 미승인 도시 행정자료는 이 공개 저장소에 저장하지 않습니다. 이 리서치 저장소의 라이선스는 아직 지정하지 않았습니다. 공모전 제출용 오픈소스 코드의 라이선스는 별도로 결정해야 합니다.