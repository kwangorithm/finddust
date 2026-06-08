# FindDust

안양대학교 일반대학원 환경공학과 미세먼지관리전공 석사생을 위한 디지털 연구 도구 특강 자료입니다. Git/GitHub, AI 코딩 도구, Overleaf, 참고문헌 관리, 논문 방법론 보조자료를 5세션 흐름으로 연결합니다.

## 사이트

- GitHub Pages: https://kwangorithm.github.io/finddust/
- 로컬 미리보기: `python3 -m http.server 8000`

## 슬라이드

| 세션 | 주제 | 페이지 |
|---:|---|---|
| 1 | Git & GitHub 기초 | [`session1-slides.html`](session1-slides.html) |
| 2 | GitHub 협업 | [`session2-slides.html`](session2-slides.html) |
| 3 | Claude Code | [`session3-slides.html`](session3-slides.html) |
| 4 | OpenAI Codex & 고급 AI 도구 | [`session4-slides.html`](session4-slides.html) |
| 5 | Overleaf & 참고문헌 관리 | [`session5-slides.html`](session5-slides.html) |

## 논문 방법론 보조자료

| 자료 | 설명 | 페이지 |
|---|---|---|
| Research Method | 주제 좁히기, 키워드 확장, 검색식, 초록 스크리닝, Research Gap 도출 | [`research-method.html`](research-method.html) |
| Templates | 논문 목록, 키워드 맵, 스크리닝 로그, Reference Matrix, 재현성 체크리스트 | [`templates.html`](templates.html) |
| Prompts | 키워드 확장, 초록 스크리닝, 논문 요약, Research Gap 검증, Introduction 피드백 | [`prompts.html`](prompts.html) |
| Final Project | 최종 논문 초안 패키지 제출물과 루브릭 | [`final-project.html`](final-project.html) |

## 복사용 Markdown 파일

- [`templates/paper_list.md`](templates/paper_list.md)
- [`templates/keyword_map.md`](templates/keyword_map.md)
- [`templates/screening_log.md`](templates/screening_log.md)
- [`templates/paper_summary_template.md`](templates/paper_summary_template.md)
- [`templates/reference_matrix.md`](templates/reference_matrix.md)
- [`templates/claim_evidence_matrix.md`](templates/claim_evidence_matrix.md)
- [`templates/research_gap_template.md`](templates/research_gap_template.md)
- [`templates/introduction_template.md`](templates/introduction_template.md)
- [`templates/reproducibility_checklist.md`](templates/reproducibility_checklist.md)
- [`prompts/keyword_expansion_prompt.md`](prompts/keyword_expansion_prompt.md)
- [`prompts/abstract_screening_prompt.md`](prompts/abstract_screening_prompt.md)
- [`prompts/paper_summary_prompt.md`](prompts/paper_summary_prompt.md)
- [`prompts/reference_comparison_prompt.md`](prompts/reference_comparison_prompt.md)
- [`prompts/research_gap_prompt.md`](prompts/research_gap_prompt.md)
- [`prompts/research_gap_validation_prompt.md`](prompts/research_gap_validation_prompt.md)
- [`prompts/introduction_writing_prompt.md`](prompts/introduction_writing_prompt.md)
- [`prompts/introduction_critical_feedback_prompt.md`](prompts/introduction_critical_feedback_prompt.md)

## Windows 수강생 체크리스트

1. Git for Windows 설치: https://git-scm.com/download/win
2. 시작 메뉴에서 `Git Bash` 실행
3. 아래 설정 확인:

```bash
git --version
git config --global user.name "홍길동"
git config --global init.defaultBranch main
git config --global core.autocrlf true
git config --list
```

첫 `git push` 때 GitHub 로그인 창이 뜨면 브라우저 인증을 완료합니다. 이후 인증은 Git Credential Manager가 저장합니다.

## 최종 산출물

1. GitHub `pm25-thesis` 저장소
2. 논문 10편 이상 레퍼런스 목록
3. 논문 요약 카드 5개 이상
4. Reference Matrix
5. Research Gap 문서
6. Introduction 5문단 초안
7. Figure 1개 이상과 재현 가능한 분석 코드
8. Overleaf PDF 초안
