# Interstellar War — Story Bible Wiki

스페이스 오페라 웹소설 **《Interstellar War》**의 설정집(스토리 바이블) 위키.

Andrej Karpathy의 **LLM Wiki** 패턴을 차용함 — 자료를 질문할 때마다 다시 읽는 대신,
**수집(ingest) 시점에 설정을 위키로 컴파일**하고 집필이 진행될수록 복리(compounding)로
세계관을 축적함. LLM(Claude)이 마크다운 문서를 직접 작성·편집·연결하는 **위키 에디터
(설정 관리자)** 역할을 함.

> 작업 규약·스키마의 단일 출처(SSOT)는 [`CLAUDE.md`](CLAUDE.md)임. 이 README는 개요만 제공함.

---

## 3-레이어 아키텍처

| 레이어 | 위치 | 소유자 | 변경 규칙 |
|--------|------|--------|-----------|
| **Raw sources** | `sources/` | 사람 | 불변(immutable). LLM은 읽기만 함. |
| **Wiki** | 엔티티 폴더 (`00_~06_`) | LLM | LLM이 생성·갱신·연결함. |
| **Schema** | `CLAUDE.md` | 사람+LLM | 규약을 정의함. |

원본(작가 메모·집필 원고·참고 자료)은 `sources/`에 그대로 보존하고, 그 가공물(정리된
설정)만 위키 레이어에 둠.

## 디렉토리 구조

```
/
├── CLAUDE.md         # 스키마/작업 지침 (SSOT)
├── sources/          # 원본(불변) 레이어 — 텍스트 원본 + sources/files/ 바이너리
├── 00_Index/         # 목차·지도(MOC)·연표·관계도
├── 01_Characters/    # 인물 — 프로필·동기·관계·아크
├── 02_Factions/      # 세력 — 국가·제국·진영·조직·함대·기업
├── 03_Locations/     # 장소 — 항성계·행성·정거장·함선·전장
├── 04_Lore/          # 세계관 — 기술·과학설정·역사·종교·문화·용어집
├── 05_Plot/          # 플롯 — 아크·회차 노트·복선·사건 추적
├── 06_Logs/          # log.md (append-only) + 작업 일지
└── assets/           # 위키 레이어 미디어 — 지도·삽화·도표
```

## 핵심 원칙

1. **3-레이어 분리** — 불변 원본 · LLM 소유 위키 · 스키마.
2. **LLM이 설정 관리자** — 설정/장면/자료를 던지면 Claude가 문서를 생성·갱신함.
3. **복리 축적** — 집필·질의를 거듭하며 세계관을 보강함.
4. **출처 추적(provenance)** — 모든 설정은 `sources/`의 source-id로 역추적 가능.
5. **Atomic Notes** — 한 파일에 한 엔티티. 파일명이 곧 제목.
6. **정합성(canon) 우선** — 설정 충돌은 모순 블록으로 보존, 확정 설정은 명확히 표시.
7. **한국어 우선** — 문서는 한국어로 작성, 고유명사·기술 용어는 영문 병기 가능.

## 워크플로 요약

- **수집(Ingest)** — 새 소스를 `sources/`에 추가·등록 → 핵심 엔티티 추출 → 관련 위키
  페이지 갱신/생성 → `[[ ]]`로 상호 연결 → MOC·log 등록.
- **질의(Query)** — MOC에서 관련 페이지 탐색 → 인용과 함께 답 합성 → 새 합성 결과는
  `type: answer` 페이지로 위키에 환원.

자세한 규칙은 [`CLAUDE.md`](CLAUDE.md)와 [`sources/README.md`](sources/README.md) 참고.

## 사용 도구

- **편집기** — [Obsidian](https://obsidian.md/) (wikilink·그래프뷰 호환).
- **설정 관리자** — [Claude Code](https://claude.com/claude-code) (LLM 위키 에디터).
