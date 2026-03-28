# 상세페이지 AI 제작 에이전트

이커머스 식품 상세페이지를 자동 제작하는 Claude Code 에이전트입니다.

## 실행

```
/detail-page
```

## 구조

- `.claude/commands/detail-page.md` — 메인 스킬 (6단계 프로세스)
- `scripts/gemini-image.py` — Gemini 이미지 생성 (플랫폼별 규격)
- `templates/detail-base.html` — HTML 템플릿
- `prompts/` — 4가지 스타일 + 16개 블록 프롬프트
- `output/` — 생성 결과물

## 지원 플랫폼

| 플랫폼 | 이미지 가로폭 |
|--------|-------------|
| 쿠팡 | 780px |
| 네이버 스마트스토어 | 860px |
| 올웨이즈 | 720px |
| 토스 쇼핑 | 860px |
| 공통 호환 | 860px |

## 프로세스

```
Phase 0: 초기 설정 (API 키 자동 확인 + 플랫폼 + 입력 모드 + 스타일)
Phase 1: 상품 정보 수집
Phase 2: 병렬 분석 (타겟 + 경쟁 + USP — 3개 동시)
Phase 3: 블록 설계 + 카피라이팅
Phase 4: 이미지 생성 (Gemini)
Phase 5: 조립 + 저장
```
