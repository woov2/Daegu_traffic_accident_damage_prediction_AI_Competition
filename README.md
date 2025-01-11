# Daegu_traffic_accident_damage_prediction_AI_Competition

<br/>

## 1. 배경 & 목적

- 이동수단의 발달에 따라 다양한 유형의 교통사고들이 계속 발생.
- 사고 발생 시간, 공간 등의 정보를 활용하여 사고위험도(ECLO)를 예측하는 AI 알고리즘 개발
- 평가 지표: RMSLE

<br/>

## 2. 주최/주관 & 참가 대상 & 성과

- 주최: 산업통상자원부, 대구광역시
- 주관: 한국자동차연구원, 대구디지털혁신진흥원
- 참가 대상: 전국민
- 성과: 대구디지털혁신진흥원장상 수상(3위)

<br/>

## 3. 대회 기간

- 제출마감: 2023년 12월 11일
- 코드 평가 마감 및 최종순위 발표: 2023년 12월 19일

<br/>

## 4. 내용
- 시공간 정보 및 사고정보에 대한 데이터가 많을수록 예측 성능이 향상될 것이라 판단하여 공공데이터포털로부터 추가 데이터 수집하여 사용.
- EDA 결과, 시간별 사고위험도의 시계열성, 산간지역, 고속도로 인근 지역 등 특정 지역에서 높은 사고위험도, CCTV 제한속도가 사고위험도과 연관
- 3가지 가설 설정을 통한 Feature Engineering(공간적 특성 / 사고다발구역 / 시간적 특성)
- 공간정보(범주형 변수) = Catboost, 시간정보(시계열 변수) = XGBoost
- Weighted Ensemble

<br/>

## 5. Process

### ch.1 Feature Engineering

-  EDA
- Groupby Features
- Target Features
- Time Features(Seasonal, Cycling Transform)

---

### ch.2 Preprocessing

- NAN processing
- City Regrouping
- External Data preprocessing
- Categoryical to Numeric Transform(Label Encoding)

---

### ch.3 Modeling

- Catboost(Tuning)
- XGBoost(Tuning)

---

### ch.4 Ensemble

- Weighted Ensemble
- Catboost 5 : XGBoost 5

<br/>

## 6. 참고자료

[대구 교통사고 피해 예측 AI 경진대회 사이트]([https://www.kaggle.com/competitions/2021-daplatformers-final-round/overview](https://dacon.io/competitions/official/236193/overview/schedule)
