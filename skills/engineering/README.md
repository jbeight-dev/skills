# engineering

## Diagnose - 원인을 체계적으로 진단한다.
문제를 “문서”가 아니라 “실행 가능한 형태”로 남긴다

“감으로 디버깅하지 말고, 재현 가능한 루프를 먼저 만든 뒤 과학적으로 원인을 좁혀가라”
라는 디버깅 방법론입니다.

- 좋은 디버깅 = 좋은 재현 루프 만들기


| 단계 | 목적 |
|--|--|
| Phase 1 | 재현 루프 만들기 |
| Phase 2 | 실제 버그 재현 |
| Phase 3 | 가설 수립 |
| Phase 4 | 로그/디버깅으로 검증 |
| Phase 5 | 수정 + 회귀 테스트 |
| Phase 6 | 정리 + 사후 분석 |


예를 들어 "catalog share 후 조회가 안됩니다."
- 재현 루프 만들기
1. catalog 생성
2. share API 호출
3. /v1/catalogs 조회
4. 결과 검증

코드 수정
→ test-share-flow.sh 실행
→ 바로 PASS/FAIL 확인