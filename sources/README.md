# sources/ — Raw Sources (불변 레이어)

여기에는 위키의 **원본 자료**를 둔다. 사람이 큐레이션하며, LLM은 **읽기만** 한다.
(원본은 절대 수정하지 않는다. 설정 정리/가공은 위키 엔티티 폴더에서 이뤄진다.)

소설 위키에서 원본이란: **작가 메모·설정 초안·집필 원고·참고한 실제 과학/역사/
신화 자료·레퍼런스 이미지 설명** 등을 가리킨다.

## 등록 규칙

- 각 소스는 고유한 **source-id** (kebab-case) 를 가진다. 예: `author-memo-2026-06`.
- **텍스트 원본**(메모·원고)은 `sources/` 에 `.md` 로 직접 둔다(`manuscript-ep01.md`).
- **바이너리 원본**(PDF·스캔·이미지 자료)은 `sources/files/` 에 둔다(파일명에 source-id 사용 권장).
- **외부 링크**(웹·논문 URL)는 파일 없이 아래 표에만 등록한다.
- 어느 경우든 아래 인덱스 표에 한 줄 등록하고, 위치/URL 칸에 실제 경로 또는 링크를 적는다.
- 위키 페이지의 `sources:` frontmatter 와 본문 `(출처: source-id)` 가 이 id 를 참조한다.

## 소스 인덱스

| source-id | 제목 | 유형 | 위치/URL | 추가일 |
|-----------|------|------|----------|--------|
| bryson-2020-kepler-gaia | NASA Kepler+Gaia 분석 (Bryson et al. 2020) — 태양형 별 거주가능 행성 ≥3억 개 | web/paper | https://www.cnn.com/2020/11/05/world/nasa-300-million-habitable-planets-intl-hnk-scli-scn | 2026-06-04 |
| petigura-2013-pnas | Petigura et al. 2013, PNAS — 태양형 별의 22%가 거주가능대 지구형 행성 보유 | paper | https://www.pnas.org/doi/10.1073/pnas.1319909110 | 2026-06-04 |
| berkeley-2013-news | UC Berkeley 보도 — 거주가능 행성은 흔한가 (적색왜성 포함 시 ~400억) | web | https://news.berkeley.edu/2013/11/04/astronomers-answer-key-question-how-common-are-habitable-planets/ | 2026-06-04 |
| chatgpt-dstage-civ | D단계: 시공간공학 문명 (ChatGPT로 정리한 세계관 기술체계 설정) | pdf | files/D단계 시공간공학 문명.pdf | 2026-06-04 |
