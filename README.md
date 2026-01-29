![Python](https://img.shields.io/badge/python-3.11+-blue.svg)
![XGBoost](https://img.shields.io/badge/XGBoost-0.91_AUC-orange.svg)
![Stats](https://img.shields.io/badge/Statistics-Regression-green.svg)
![LightGBM](https://img.shields.io/badge/LightGBM-0.90_AUC-yellow.svg)
![Stats](https://img.shields.io/badge/Statistics-Logit%20%26%20Tests-green.svg)
![EDA](https://img.shields.io/badge/EDA-Visualization-red.svg)



# 프로젝트 주제 : 학생 시험 점수 예측 분석 프로젝트

### 🚀 핵심 성과 (Key Highlights)
- **데이터 분석** : 13개 변수 중 11개의 핵심변수를 (study_hours, class_attendance 등) 기반으로 한 다각도 통계 검정 수행
- **최고 성능 달성** : XGBoost 를 통해 **결정계수 0.9245**기록 , **MAE 오차 2.14**기록

## ✔️1. project overview
- **주제** : 학습 패턴 데이터를 활용한 성취도 예측 및 영향요인 분석
- **데이터셋** : [Exam score prediction dataset](https://www.kaggle.com/competitions/playground-series-s6e1/data)
- **프로젝트 기간** 26.1.28~26.1.30

- **핵심 목표** : `학생들의 학습 행동 데이터`를 활용하여 시험 점수를 예측하고 점수에 가장 큰 영향을 미치는 요인 파악 

## ✔️2. Data Dictionary (주요 핵심 변수)
- 실제 분석 결과 통해 확보한 변수들의 내용 기재
- 총 변수갯수 : 13개 中 11개 핵심변수 선정

| 변수명 | 설명 | 변수 유형 |
| :--- | :--- | :--- |
| **id** | 각 학생의 고유 식별 번호(0, 1, 2...) | 숫자형 (제외대상) |
| **age** | 학생의 나이 (17세 ~ 24세) | 수치형 (Continuous) |
| **study_hours** | 하루 평균 공부 시간(0 ~ 10시간 사이) | 수치형 (Continuous) | **핵심 연속형**
| **class_attendance** | 출석률(0 ~ 100%) | 수치형 (Continuous) | **핵심 연속형**
| **sleep_hours** | 수면 시간(4 ~ 10시간 사이) | 수치형 (Continuous) |
| **exam_score** | 시험 점수(Target) | 수치형 (Continuous) | **예측 목표**
| **gender** | 성별(female, male, other) | 범주형(Binary) |
| **course** | 수강 과목(b.sc, bca, ba, b.com, b.tech, diploma) | 범주형(Binary) |
| **internet_access** | 인터넷 사용 가능 여부(yes, no) | 범주형(Binary) |
| **sleep_quality** | 수면의 질(poor, average, good) | 범주형 (Binary) |
| **study_method** | 주요 학습 방법(self-study, coaching, mixed등) | 범주형 (Binary) |
| **facility_rating** | 시설 만족도(low, medium, high) | 범주형 (Binary) |
| **exam_difficulty** | 시험 난이도(easy, moderate, hard) | 범주형 (Binary) |