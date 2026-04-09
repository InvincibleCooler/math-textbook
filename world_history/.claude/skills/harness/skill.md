---
name: harness
description: "세계사 학습 하네스. 에이전트와 스킬을 조율하여 학습 콘텐츠를 생성."
---

# World History Harness - 하네스 구성 복사본

이 프로젝트 전용 하네스. 상위 하네스(`~/.claude/skills/harness`)를 상속.
세계사 학습 콘텐츠 생성에 특화된 에이전트 팀을 관리.

## 에이전트 팀 구성

| 에이전트 | 역할 | 스킬 |
|----------|------|------|
| `treaty-analyst` | 조약 분석 전문가 | `treaty-summary`, `treaty-book` |

## 시나리오별 호출

| 사용자 요청 | 호출 대상 |
|-------------|-----------|
| "베스트팔렌 조약 정리해줘" | `treaty-analyst` + `treaty-summary` |
| "조약 책 만들어줘" | `treaty-analyst` + `treaty-book` |
| "근세 조약 정리" | `treaty-analyst` + `treaty-book` (범위: 근세) |

## 확장 계획
- `era-analyst`: 시대별 배경 분석 에이전트 (추후)
- `exam-quiz`: 수능 기출 문제 생성 스킬 (추후)
- `figure-analyst`: 인물 분석 에이전트 (추후)