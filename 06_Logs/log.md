# Wiki Log

append-only. 최신 항목을 아래에 추가함. 포맷: `YYYY-MM-DD | <작업유형> | <대상> | <설명>`

2026-06-01 | MAINT | repo | LLM Wiki 초기 골격 구축 (CLAUDE.md, sources/, wiki/)
2026-06-01 | INGEST | karpathy-llm-wiki-gist | 원본 gist 수집 → [[LLM Wiki]] 생성, [[RAG]]/[[Andrej Karpathy]] stub 등록
2026-06-01 | MAINT | repo | CLAUDE.md 통합본 작성 (03 기반 + 02 규약 흡수, PARA 6폴더 유지)
2026-06-01 | MAINT | repo | PARA 구조로 마이그레이션 (wiki/ → 00_Index/01_Concepts/03_References/05_Logs), frontmatter·wikilink 갱신
2026-06-01 | INGEST | rag-paper-lewis-2020 | RAG 원 논문 수집 → [[RAG]] draft 보강(구성요소·정식화·한계), [[DPR]]/[[BART]] stub 링크 생성
2026-06-01 | INGEST | karpathy-wikipedia | Karpathy 위키 수집 → [[Andrej Karpathy]] draft 보강(학력·경력 타임라인·기여)
2026-06-01 | INGEST | dpr-paper-karpukhin-2020 | DPR 원 논문 수집 → [[DPR]] 페이지 생성(draft), MOC stub 해소
2026-06-01 | INGEST | bart-paper-lewis-2019 | BART 원 논문 수집 → [[BART]] 페이지 생성(draft), MOC stub 해소
2026-06-04 | MAINT | repo | 용도 전환 — LLM 지식 위키 → 스페이스 오페라 소설 설정집(스토리 바이블)
2026-06-04 | MAINT | repo | 더미 콘텐츠 삭제 (RAG/BART/DPR/LLM Wiki/Karpathy 페이지 + 동명 sources)
2026-06-04 | MAINT | repo | 폴더 재구성: PARA → 01_Characters/02_Factions/03_Locations/04_Lore/05_Plot, 05_Logs→06_Logs
2026-06-04 | MAINT | CLAUDE.md | 스키마 개정 (제목·원칙·디렉토리·frontmatter type/status·로그 경로 소설용으로 교체)
2026-06-04 | UPDATE | 00_Index/MOC.md, sources/README.md | 소설 위키용으로 재작성, 더미 소스 인덱스 비움
2026-06-04 | INGEST | bryson-2020-kepler-gaia, petigura-2013-pnas, berkeley-2013-news | 은하 거주가능 행성 수 자료 3건 수집·등록
2026-06-04 | QUERY | 은하 거주가능 행성 수 | 웹 조사 → [[은하 내 거주가능 행성 수 추정]] answer 페이지 환원(draft), MOC 등록
2026-06-04 | MAINT | 세계관 톤 | 톤=광활한 스페이스 오페라, 거주가능 후보 앵커=보수치 3억 개 확정
2026-06-04 | QUERY | 즉시 거주가능 행성 수 | 3억→필터 캐스케이드로 에덴급 ≈9만 개(0.03%) 산출 → [[즉시 거주가능 행성 수 추정]] 환원(draft), MOC 등록
2026-06-04 | CREATE | 기술 수준 (분야별) | 인공중력 키스톤 기반 분야별 기술등급(T3) 정리, 결정포인트 5개 명시 → [[기술 수준 (분야별)]] draft, MOC 등록
2026-06-04 | MAINT | sources/assets 정책 | 종속 관리 확정 — 출처 바이너리=sources/files/, 위키 미디어=assets/. sources/files/ 생성, CLAUDE.md(3·9)·sources/README.md 규칙 갱신
2026-06-04 | INGEST | chatgpt-dstage-civ | "D단계 시공간공학 문명" PDF(22p) 수집 → [[D단계 시공간공학 문명]](기술체계 SSOT)·[[행성 분류 체계 (A~E급)]] 생성(stable), 소스 등록
2026-06-04 | UPDATE | 기술 수준 (분야별) | PDF 캐논 정렬 — 결정포인트 5개 중 3해소(FTL/통신/동력)·2갱신(AI·죽음). D단계 페이지로 흡수 표기
2026-06-04 | UPDATE | 거주가능/즉시거주가능 행성 | A~E급 연결(에덴급=A급) 추가, 상호 검증, MOC 갱신
2026-06-08 | MAINT | repo | git init(main)·.gitignore 추가, GitHub 원격(JoSangyeon1983/interstellar-war) 연결, 초기 커밋(2fa86eb) 푸시
2026-06-08 | CREATE | README.md | 루트 README 작성 (프로젝트 개요·3레이어·디렉토리·원칙·워크플로), CLAUDE.md를 SSOT로 명시
