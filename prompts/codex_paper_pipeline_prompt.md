# Codex 붙여넣기용 프롬프트: PM2.5 논문 산출물 파이프라인

당신은 연구 보조 에이전트입니다. 이 저장소를 읽고, PM2.5 분석 결과를 논문 초안에 바로 연결할 수 있도록 코드·그림·표·문서 산출물을 생성해 주세요.

## 목표

`python src/analyze_pm25.py` 명령 한 번으로 다음 산출물이 생성되어야 합니다.

- `figures/pm25_monthly_trend.png`
- `tables/summary_stats.tex`
- `docs/result_summary.md`

또한 `README.md`에 실행 방법과 산출물 설명을 추가해 주세요.

## 입력 데이터

- 입력 파일: `data/sample_pm25.csv`
- 먼저 CSV의 컬럼명을 확인하고, 날짜 컬럼과 PM2.5 농도 컬럼을 합리적으로 추정해 주세요.
- 컬럼명이 애매하면 코드 상단에 주석으로 가정한 컬럼명을 명시해 주세요.
- 결측치와 비수치 값은 분석 전에 안전하게 처리해 주세요.

## 생성/수정할 파일

### 1. `src/analyze_pm25.py`

다음 기능을 포함해 주세요.

1. `data/sample_pm25.csv` 읽기
2. 날짜 컬럼을 datetime으로 변환
3. PM2.5 농도 컬럼을 numeric으로 변환
4. 월별 평균 PM2.5 계산
5. 기본 요약통계 계산: count, mean, std, min, median, max
6. `figures/pm25_monthly_trend.png` 저장
   - x축: 월
   - y축: PM2.5 concentration (µg/m³)
   - 제목과 축 라벨 포함
   - 가능하면 기준선 또는 평균선 포함
7. `tables/summary_stats.tex` 저장
   - LaTeX에서 `\input{tables/summary_stats.tex}`로 삽입 가능한 표
   - 가능하면 `booktabs` 스타일 사용
8. `docs/result_summary.md` 저장
   - 데이터 기간
   - 관측치 수
   - 평균/최소/최대/중앙값
   - 월별 추세에 대한 Results 문단 초안
   - Figure와 Table을 논문에서 어떻게 인용할지 예시 문장
9. 필요한 폴더가 없으면 자동 생성
10. 실행 완료 후 생성 파일 경로를 터미널에 출력

### 2. `README.md`

다음 내용을 추가해 주세요.

- 필요한 Python 패키지
- 실행 명령: `python src/analyze_pm25.py`
- 생성되는 산출물 목록
- Overleaf에 업로드할 파일 목록

## 구현 조건

- 상대경로는 저장소 루트 기준으로 동작하게 해 주세요.
- 한글 환경이 아니어도 실행되도록 그래프의 기본 텍스트는 영어로 작성해 주세요.
- 오류가 발생하면 어떤 파일/컬럼이 문제인지 알 수 있도록 명확한 메시지를 출력해 주세요.
- 임의의 분석 결과를 꾸며내지 말고 반드시 CSV에서 계산한 값만 사용해 주세요.
- 변경 후 가능하면 직접 `python src/analyze_pm25.py`를 실행해 보고 오류를 수정해 주세요.
