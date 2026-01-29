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
| **study_hours** | 하루 평균 공부 시간(0 ~ 10시간 사이) | **수치형 (Continuous)****핵심연속형** | 
| **class_attendance** | 출석률(0 ~ 100%) | **수치형 (Continuous)****핵심연속형** | 
| **sleep_hours** | 수면 시간(4 ~ 10시간 사이) | 수치형 (Continuous) |
| **exam_score** | 시험 점수(Target) | **수치형 (Continuous)****예측목표** | 
| **gender** | 성별(female, male, other) | 범주형(Binary) |
| **course** | 수강 과목(b.sc, bca, ba, b.com, b.tech, diploma) | 범주형(Binary) |
| **internet_access** | 인터넷 사용 가능 여부(yes, no) | 범주형(Binary) |
| **sleep_quality** | 수면의 질(poor, average, good) | 범주형 (Binary) |
| **study_method** | 주요 학습 방법(self-study, coaching, mixed등) | 범주형 (Binary) |
| **facility_rating** | 시설 만족도(low, medium, high) | 범주형 (Binary) |
| **exam_difficulty** | 시험 난이도(easy, moderate, hard) | 범주형 (Binary) |

 ## ✔️3. Problem Definition
 **3.1 데이터 특성 및 분석 과제**<br>
 - **현상** : 평균 근처에만 몰려있는 것이 아니라 점수 편차가 꽤 크다는 것을 보여줌<br>
 - **대응** : 학생들 간 실력 차이가 존재하므로 맞춤형 학습 지원이 필요하다는 통계적 근거<br>
 ![주요 변수 구조 시각화](/output/EDA.png)

 - **복합적 요인성**<br>
    + **현상** : 공부 시간(주요 동인), 출석률 & 인터넷 접근성(환경적 매개요인), 수면시간(신체적 기초요인)
    + **대응** : 변수 간 단순 선형관계를 넘어, 고차원 알고리즘 적용이 필수적<br>

 **3.2 분석 전략 및 방법론**<br>
 - **통계 분석** : 다변량 상관계수 분석, 탐색적 데이터 분석(EDA), 유의성 검정(P-value), VIF 분석<br>
 - **머신 러닝** : Random forest, Hyperparameter Tuning, XGBoost, MAE, SHAP<br>

## ✔️4. Data preprocessing
- **범주형 변수 처리** 
    + **성별**,**수강과정**,**학습방법**,**인터넷**

## ✔️5. 통계분석 핵심 인사이트 (연속형 + 범주형)
- **[Study_hours]**, **[Attendance]**, **[Sleep_hours]** 연속형 변수 인사이트
- **[Internet_access]**, **[Study_method]**, **[Sleep_quality]** 범주형 변수 인사이트
- **충분한 학습 시간이 뒷받침된 상태에서 수면의 질, 효율적인 학습 방법이 결합될 때 비로소 고득점으로 이어지는 `시너지 효과`가 발생합니다**


##











