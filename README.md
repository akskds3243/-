#  SECOM Semiconductor Wafer Fault Analysis & Auto SPC Dashboard

반도체 웨이퍼 공정 데이터(UCI SECOM)를 활용하여 불량 원인 센서를 자동 도출하는 **Machine Learning Pipeline**과 6시그마 통계적 공정 제어를 위한 **Auto SPC Control Dashboard**를 구현한 포트폴리오 프로젝트입니다.

---

##  Key Features

### 1. Auto ML Pipeline (`Auto_SECOM_ML.py`)
- **범용 타겟 & 센서 자동 감지**: 데이터셋 구조 변경 시 타겟(불량) 열 및 ID/시간 열 자동 인식
- **전처리 자동화**: 결측치 중앙값 대치 및 분산 0인 무의미 센서 자동 제거
- **특성 선택 (Feature Selection)**: `SelectKBest` (ANOVA F-value) 기반 핵심 영향을 미치는 Top 센서 도출
- **불균형 데이터 대응**: `SMOTE` 오버샘플링을 적용하여 소수 클래스(불량 웨이퍼) 예측 성능 최적화
- **분류 모델**: `RandomForestClassifier` 기반 불량 예측 및 평가 리포트 출력




