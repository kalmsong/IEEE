# 공식 자료 및 근거 목록

**조사일: 2026-11-12**. 해당 URL은 원문 출처이며 문서 내용은 이후 변경될 수 있다. 원문 PDF·상표 이미지는 이 저장소에 복제하지 않고 링크로 참조한다.

| ID | 출처 | 확인한 내용 | 확인 상태 |
|---|---|---|---|
| S01 | [IEEE 공모전 메인](https://ieeeht.org/get-involved/funding-opportunities/genai-for-good/) | 기획 의도, 참가 조건, GENIE 현행 모집페이지의 필수 문구, 1차 제출물, 평가 기준·마감 | 공개 페이지 직접 확인 |
| S02 | [스코페 공식 과제 PDF](https://ieeeht.org/wp-content/uploads/2026/11/GAI4GC-Cities-Edition-Use-Case-Green-Infrastructure-AI-Assistant-Skopje-North-Macedonia.pdf) | MVP 4종, GIS·인허가 자료, 전문가 승인, 시범지역 자료 미확정 | PDF 4p 확인 |
| S03 | [리브네 공식 과제 PDF](https://ieeeht.org/wp-content/uploads/2026/11/GAI4GC-Cities-Edition-Use-Case-Energy-Advisory-AI-Assistant-Rivne-Ukraine.pdf) | MVP 4종, 건물자료·에너지 기준, 개략 추정, 보고서 | PDF 6p 확인 |
| S04 | [Zindi 공모전 규정](https://zindi.world/competitions/GenAI-for-Good-Challenge) | 모델 제한, 기술 점수, 숨겨진 시험, 코드 재현성 | 공개 페이지 직접 확인 |
| S05 | [Zindi 자료 페이지](https://zindi.world/competitions/GenAI-for-Good-Challenge/data) | 공개 파일 목록과 파일 설명, 허용 데이터·자료 구분 | 공개 목록 확인 + 별도 대화 내 파일 수령 |
| S06 | [ITU GENIE 소개](https://www.itu.int/itu-d/sites/genieai/) | 공공기관용 오픈소스 AI 플랫폼 개념 | 공개 링크 |
| S07 | [GENIE 개발 문서](https://genie-ai-7e342b.opensource.unicc.org/docs/get-started/welcome/) | 설치·RAG·모델 구성 가이드 | 공개 링크 |
| S08 | [스코페 녹지 ArcGIS](https://gisportal.skopje.gov.mk/arcgis/rest/services/ZK/Drva_grmuski_app/MapServer) | 공개 서비스 URL | 실제 시범데이터 패키지와 별개 |

## 아직 확보하지 못한 자료

- `Train.csv`, `Test.csv`, `SampleSubmission.md`, `StarterNotebook.ipynb`의 **실제 파일 내용**.
- 원천자료 묶음의 실제 파일 구조·라이선스 메타데이터·건수.
- 스코페 시범지역 행정문서·정식 GIS 추출본 및 열람 권한.
- 리브네 건물별 원본 정보·실제 에너지 진단·적용 계산 기준·비용 DB.

실제 확보 전에는 예시 데이터로 만든 도식임을 표시해야 하며, 실증 가능성의 근거로 취급하지 않는다.\n\n## GENIE 사전 테스트 근거\n\n- [GENIE 로컬 설치 퀵스타트](https://genie-ai-7e342b.opensource.unicc.org/docs/get-started/quickstart-deployer/): Docker Compose, core/opea/GPU 구분, `/api/health`, Keycloak 로그인.\n- [GENIE 설치](https://genie-ai-7e342b.opensource.unicc.org/docs/deploy/install-guide/): 기본 사양 및 환경설정.\n- [GENIE 실행 시나리오](GENIE_QA_AND_TEST_PLAN.md): 문서 기반 사전 검증 계획. 실설치 수행 여부는 별도 상태 관리.\n