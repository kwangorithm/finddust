# PM2.5 논문 프로젝트 폴더 구조

아래 구조는 Codex로 분석 산출물을 만들고 Overleaf에서 논문 PDF 초안을 조립하기 위한 기본 구조입니다.

```text
pm25-paper-project/
├── data/
│   └── sample_pm25.csv
├── src/
│   └── analyze_pm25.py
├── figures/
│   └── pm25_monthly_trend.png
├── tables/
│   └── summary_stats.tex
├── docs/
│   └── result_summary.md
└── paper/
    ├── main.tex
    └── references.bib
```

## 폴더별 역할

- `data/`: 원자료 또는 수업용 샘플 데이터가 들어갑니다. 원자료는 직접 수정하지 않습니다.
- `src/`: 데이터를 읽고 분석 산출물을 생성하는 Python 코드가 들어갑니다.
- `figures/`: 논문에 삽입할 그림 파일이 생성됩니다.
- `tables/`: Overleaf에서 `\input{}`으로 불러올 LaTeX 표 파일이 생성됩니다.
- `docs/`: 결과 요약, AI 사용 기록, 연구 노트 등 사람이 검토할 문서가 들어갑니다.
- `paper/`: Overleaf에 붙여넣거나 업로드할 `main.tex`, `references.bib` 등 논문 원고 파일이 들어갑니다.

## 기본 실행 흐름

1. `data/sample_pm25.csv`를 준비합니다.
2. Codex에 `prompts/codex_paper_pipeline_prompt.md` 내용을 붙여넣습니다.
3. `python src/analyze_pm25.py`를 실행합니다.
4. `figures/pm25_monthly_trend.png`, `tables/summary_stats.tex`, `docs/result_summary.md`가 생성되었는지 확인합니다.
5. Overleaf에 `main.tex`, `references.bib`, `figures/`, `tables/`를 업로드합니다.
6. Figure, Table, Citation이 정상 컴파일되는지 확인하고 PDF 초안을 제출합니다.
