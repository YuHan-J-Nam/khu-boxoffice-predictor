# 🎬 BoxOffice Predictor

Predicting movie theater audience counts using historical patterns, seasonal demand, and competitive environment.

![header](assets/boxoffice-banner.png)

## 📌 Overview

This project aims to forecast **daily movie audience counts** based on a combination of:

- Previous audience trends
- Movie interest level
- Competitive movie lineup
- Temporal features like holidays and weekends
- Rating and review dynamics

The core model incorporates **SARIMA-based forecasting** with exogenous regressors (e.g., rating, competition, interest), which helps improve predictive accuracy by reflecting real-world movie dynamics.

## 📈 Methodology

We modeled audience demand using a formula of the form:
AudienceCount_d = α × Competition_d + Σ (β_t × AudienceCount_t + γ_t × Interest_t) + δ × MovieNeed_d + θ × Rating_d + ε_d

Here, `MovieNeed` is forecasted with: MovieNeed_t = SARIMA(p,d,q)(P,D,Q)_s + β × Exog_t

Temporal variables such as **holiday, weekend, and vacation effects** are also encoded.

## 🛠️ Tech Stack

- Python (pandas, statsmodels)
- SARIMA modeling with exogenous variables
- Data preprocessing & visualization

# 🎬 BoxOffice Predictor

영화 관람객 수요를 다양한 요인을 바탕으로 예측하는 프로젝트입니다.

![header](assets/boxoffice-banner.png)

## 📌 프로젝트 개요

본 프로젝트는 **일별 영화 관람객 수요**를 예측하기 위한 모델을 구축하는 것을 목표로 합니다. 다음과 같은 변수들을 종합적으로 고려하여 예측 모델을 설계하였습니다:

- 과거 관람객 수 변화
- 영화에 대한 관심도
- 경쟁 영화의 존재 여부
- 요일, 휴일, 방학 여부 등 시간 특성
- 영화 평점과 리뷰 관련 지표

핵심 모델은 **SARIMA(계절 ARIMA)** 기반의 시계열 모델에 외생 변수(Exogenous variables)를 결합하여, 영화 수요의 시계열성과 외부 요인을 동시에 반영합니다.

## 📈 예측 방식

다음과 같은 형태의 수식을 기반으로 관람객 수요를 계산합니다:
AudienceCount_d = α × Competition_d + Σ (β_t × AudienceCount_t + γ_t × Interest_t) + δ × MovieNeed_d + θ × Rating_d + ε_d

이때 `MovieNeed`는 SARIMA 기반 시계열 모델로 예측하며, 다음과 같은 외생 변수를 포함합니다:
MovieNeed_t = SARIMA(p,d,q)(P,D,Q)_s + β × (휴일, 년도 계절성)

## 🛠️ 사용 기술

- Python (pandas, statsmodels 등)
- SARIMA 시계열 모델
- 시계열 전처리 및 시각화

## 🖼️ Example Plot (예측 결과 예시)

![prediction example](assets/prediction-example.png)

## 🧑‍💻 Authors (팀원)

- 남유한, 김윤섭, 김채원, 박시현
