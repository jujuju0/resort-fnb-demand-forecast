# Resort FnB Weekly Demand Forecast

## 0. Project Overview

### Repo Structure

```
resort-fnb-demand-forecast/
│
├─ README.md
│
├─ data/
│   ├─ raw/                     # 원본 데이터 (절대 수정 X)
│   ├─ processed/               # 전처리 완료 데이터
│   └─ external/                # (선택) 날씨, 행사 등 외부 데이터
│
├─ notebooks/
│
├─ src/
│   ├─ config/
│   ├─ data/     # label 생성 포함
│   ├─ features/
│   ├─ models/        # naive, moving avg
│   ├─ evaluation/
│   └─ utils/
│
├─ reports/
│   ├─ figures/                 # 시각화 결과
│   └─ eda_summary.md           # EDA 요약 문서
│
├─ requirements.txt
└─ .gitignore

```

## 1. Problem Statement

- 리조트 식음업장 메뉴별 1주 수요 예측

## 2. Data Description

- 영업일자, 메뉴명, 매출수량
- 파생 feature: 요일, 시즌, 휴일

## 3. EDA Insights

- 메뉴별 희소성/변동성 차이
- 주말·시즌 효과 존재

## 4. Feature Engineering

- lag / rolling / calendar feature
- zero-heavy 메뉴 처리 전략

## 5. Modeling

- Baseline vs ML 모델 비교
- XGBoost / LightGBM

## 6. Evaluation

- MAE / RMSE
- backtesting 결과

## 7. Conclusion

- 운영 효율 개선 가능성
