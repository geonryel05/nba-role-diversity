# NBA 로스터의 역할 다양성과 팀 Net rating: 2024–25 정규시즌 30개 팀 탐색적 분석

신건렬 (가천대학교 응용통계학과, 202232033)

이 저장소에는 논문의 모든 표와 그림을 원자료에서 다시 만드는 R Markdown 코드가 들어 있다.
원자료 CSV는 Sports Reference의 자료 이용 정책에 따라 함께 배포하지 않는다.
아래 방법으로 직접 내려받으면 같은 결과가 재현된다.

## 1. 원자료 내려받기

Basketball-Reference의 각 페이지에서 표 위의 **Share & Export → Get table as CSV (for Excel)** 를 눌러
CSV 내용을 아래 이름으로 `Input_data/raw/` 폴더에 저장한다. Excel에서 열어 다시 저장하지 않는다.

| 파일 이름 | 페이지 | 표 |
|---|---|---|
| `advanced.csv` | https://www.basketball-reference.com/leagues/NBA_2025_advanced.html | Advanced |
| `per_game.csv` | https://www.basketball-reference.com/leagues/NBA_2025_per_game.html | Per Game |
| `team_rating.csv` | https://www.basketball-reference.com/leagues/NBA_2025_ratings.html | Team Ratings |

논문 분석에 쓴 파일은 2026년 6월 2–3일에 내려받았다.
코드가 행 수와 변수 합계를 비교해, 내려받은 자료가 그때와 같은지 알려 준다.

## 2. 실행하기

1. R(4.0 이상, 분석은 4.3.3)과 RStudio를 설치한다.
2. RStudio에서 `Code/run_all_analysis.Rmd`를 열고 **Knit**을 누른다.
   필요한 패키지(ggplot2, ggrepel)는 자동으로 설치된다.
3. `Code/run_all_analysis.html`이 만들어진다. 마지막 "원고 수치 대조" 표가 모두 `TRUE`이면 논문과 같은 결과다.

## 3. 폴더 구조

```
Code/run_all_analysis.Rmd          분석 전체 (논문 순서: 자료 → 방법 → 결과 → 원고 대조)
Codebook_for_input_data/codebook.csv  사용 변수와 파생 변수 설명
Input_data/raw/                    원자료 3개 (직접 내려받음, 저장소에 없음)
Input_data/processed/              코드가 만드는 추출·분석용 자료
Other Material/tables/             표 (Table 1, 2, S1–S6, 검정력)
Other Material/figures/            그림 (Figure 1, 2, S1)
```

## 자료 출처

Sports Reference LLC. (2025). 2024–25 NBA season summary [Data set]. Basketball-Reference.com.
https://www.basketball-reference.com/leagues/NBA_2025.html
