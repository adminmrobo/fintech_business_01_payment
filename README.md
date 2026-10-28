# 성공과 실패를 세는 일곱 가지 방법 — 이산확률분포

**우연의 과학통계학 · 1.1** 해설 페이지

> 똑같은 "성공 아니면 실패" 실험인데, 왜 "몇 번 성공했나"와 "언제 처음 성공했나"는 서로 다른 분포가 될까?

페이지 주소: https://adminmrobo.github.io/statistics_note_ch03_Discrete-probability-distribution_01/

박사·하루·초파리 연구원·Money-Robo 네 캐릭터와 함께 밤의 연구실 검사대에서 시험관 검사, 택배 도착, 봉인 상자 추출을 직접 돌려 보며 이산확률분포 일곱 가지를 배우는 인터랙티브 해설 페이지입니다.

## 이 페이지에서 하는 것

| 칸 | 분포 | 무엇을 세나 | 직접 돌려 보는 실험 |
|---|---|---|---|
| ① | 베르누이 시행 | 한 번의 성공(1)/실패(0) | 시험관 200개 검사, 분산 p(1−p) 곡선 |
| ② | 이항분포 B(n, p) | 정해진 n번 중 성공 수 | 로트 반복 검사, 정확히·이하·이상 확률 |
| ③ | 기하·음이항분포 | 첫(r번째) 성공까지 시행 수 | 무기억성: 3번 실패한 줄의 남은 대기 |
| ④ | 포아송분포 | 단위 시간 사건 수 | 택배 도착 세기, 잘게 쪼갠 이항과 비교 |
| ⑤ | 초기하·다항분포 | 비복원 추출 수 / 범주별 횟수 | 상자에서 꺼내기(복원/비복원), 주사위·등급 분류 |
| 대결 | 칸 다섯 개의 이항 B(5, 0.4) vs 포아송 λ = 2 | 5분당 택배 수 | 5분 구간 2,000개의 실제 빈도와 겹친 넓이로 승패 결정 |

그 밖에 대표 계산 문제 검산표(페이지가 공식으로 직접 계산), R·파이썬(scipy) 함수의 세는 법 차이 표(`dgeom` vs `geom`, `dhyper` vs `hypergeom`), 확인 퀴즈 11문항, 용어 말풍선, 지식 색인, 온톨로지·서지 꾸러미(JSON-LD·Turtle·CSV·CSL-JSON·BibTeX·RIS ZIP)가 들어 있습니다.

## 파일

```
.
├── index.html   # 해설 페이지 (HTML 파일 하나, 그림·데이터 모두 포함)
├── .nojekyll    # Jekyll 처리 끄기
└── README.md
```

- 서버, 설치, 외부 라이브러리가 필요 없습니다. 외부 요청은 글꼴(IBM Plex Sans KR) 하나뿐입니다.
- `index.html`을 내려받아 더블클릭해도 그대로 열립니다.

## GitHub Pages로 공개하기

1. 저장소 `statistics_note_ch03_-Discrete-probability-distribution_01`에 이 폴더의 파일을 모두 올립니다. `.nojekyll`(숨김 파일)도 함께 올립니다.
   ```bash
   git init
   git add .
   git commit -m "1.2 이산확률분포 공개"
   git branch -M main
   git remote add origin https://github.com/adminmrobo/statistics_note_ch03_-Discrete-probability-distribution_01.git
   git push -u origin main
   ```
2. 저장소 **Settings → Pages**에서 Source를 **Deploy from a branch**, Branch를 **main / (root)**로 고르고 Save를 누릅니다.
3. 1~2분 뒤 위 페이지 주소에서 열립니다.

## 이 페이지 인용하기

안상선 (2026). 성공과 실패를 세는 일곱 가지 방법 — 이산확률분포. 우연의 과학통계학 1.2, v1.0. https://adminmrobo.github.io/statistics_note_ch03_-Discrete-probability-distribution_01/

## 출처와 표시

- 분포 공식·성질: Wikipedia — [Bernoulli](https://en.wikipedia.org/wiki/Bernoulli_distribution), [Binomial](https://en.wikipedia.org/wiki/Binomial_distribution), [Geometric](https://en.wikipedia.org/wiki/Geometric_distribution), [Negative binomial](https://en.wikipedia.org/wiki/Negative_binomial_distribution), [Poisson](https://en.wikipedia.org/wiki/Poisson_distribution), [Multinomial](https://en.wikipedia.org/wiki/Multinomial_distribution) (2026-10-29 확인)
- R 함수: [Hypergeometric](https://search.r-project.org/R/refmans/stats/html/Hypergeometric.html), [Geometric](https://search.r-project.org/R/refmans/stats/html/Geometric.html), [NegBinomial](https://search.r-project.org/R/refmans/stats/html/NegBinomial.html)
- 계산 확인: SciPy 1.18.1 `scipy.stats`
- 캐릭터 그림: adminmrobo/fruitfly-lab-expressions (커밋 ea5da3f). 페이지 안에 넣었으므로 외부에서 불러오지 않습니다.
- 시험관 검사·택배 도착 등 시뮬레이션 데이터는 시드를 고정한 설명용 모형입니다. 실제 데이터가 아닙니다.

저자: 안상선 · AI 보조 제작

라이선스: _정해지면 적어 넣을 것_
