---
name: verb-textbook
description: "영어 핵심 동사+전치사 교재 생성. '동사 교재', '영어 교재', '챕터 작성', '전치사 교재' 시 사용."
---

# Verb & Preposition Textbook — 교재 생성 오케스트레이터

영어 핵심 동사 11개 + 전치사 45개 교재를 생성하는 통합 스킬.

## 대상 교재
- 위치: `/Users/kakaoent/textbook/english_core_verbs/`
- 동사·전치사 목록: `references/verb-list.md` 참조
- 챕터 템플릿: `references/chapter-template.md` 참조

## 교재 구조
```
english_core_verbs/
  content/
    # Part 1: 핵심 동사 (11개)
    01-get.md ~ 11-bring.md
    # Part 2: 전치사·부사 (45개, Group A~F)
    12-in.md ~ 56-except.md
    # Part 3: 조합 실전
    57-combination.md
  structure/           # 목차, 서문
  review/              # 검수 결과
  book.html
  content.js
  style.css
```

## 워크플로우

### 단일 챕터 생성
1. **Research** (verb-researcher) — 감각, 빈도, 패턴 조사
2. **Write** (verb-writer) — 챕터 템플릿 기반 집필 (짧고 핵심만)
3. **Review** (verb-reviewer) — 검수. PASS/REVISE

### 전체 교재 생성
1. 디렉토리 + 목차 생성
2. Part 1 → Part 2 → Part 3 순차 생성
3. HTML 빌드

## 에이전트 구성

| 단계 | 에이전트 | 역할 |
|------|---------|------|
| Research | verb-researcher | 리서치 |
| Write | verb-writer | 집필 |
| Review | verb-reviewer | 검수 |

패턴: **파이프라인 (Research → Write → Review)**

## 핵심 원칙
- 한국어 번역 나열이 아닌 영어 감각 중심 서술
- 짧고 단순하게, 하지만 공부는 가능하도록
- 빈도순 배치 (자주 쓰는 것부터)
- 공간 → 시간 → 추상 확장 흐름
- 동사와 전치사의 조합 연결성 강조
- 연습문제 반드시 정답 포함
- 동사 챕터 A4 2~3장, 전치사 챕터 A4 1~2장