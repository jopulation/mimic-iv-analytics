# MIMIC-IV Clinical Data Analysis & Prediction

## 🏥 Project Overview
이 프로젝트는 **MIMIC-IV Demo (v2.2)** 데이터를 활용하여 중환자실(ICU) 환자의 임상 데이터를 분석하고, 주요 헬스케어 지표를 예측하는 모델을 구축하기 위한 연구 베이스라인입니다.

**GraphCare** 논문 등 최신 의료 AI 연구에서 주로 다루는 4가지 핵심 태스크를 위한 데이터 전처리(Preprocessing) 및 탐색적 데이터 분석(EDA)을 포함합니다.

## 🎯 Key Objectives
1.  **Data Understanding:** 복잡한 EHR(Electronic Health Records) 데이터 구조 파악 및 테이블 간 관계 분석
2.  **EDA (Exploratory Data Analysis):**
    * 재원 기간 (Length of Stay, LOS) 분포 확인
    * 원내 사망률 (Mortality Rate) 분석
    * 주요 진단 코드 (ICD Codes) 빈도 분석
3.  **Preprocessing:** 시계열 데이터 정제 및 환자별 `Visit-level` 데이터 구축
4.  **Prediction (Future Work):** 사망률, 재입원, 재원 기간, 약물 추천 예측 모델 구현

## 📂 Dataset
본 프로젝트는 [PhysioNet](https://physionet.org/content/mimic-iv-demo/2.2/)의 **MIMIC-IV Clinical Database Demo (v2.2)**를 사용합니다.
* **Subjects:** 100명의 중환자 샘플 데이터
* **Modules:** `hosp` (병원 일반 기록), `icu` (중환자실 기록)
* *Note: MIMIC-IV 데이터 사용 승인을 준수하며, 원본 데이터 파일은 저장소에 포함되지 않습니다.*

## 🛠 Tech Stack
* **Language:** Python 3.9+
* **Data Manipulation:** Pandas, NumPy
* **Visualization:** Matplotlib, Seaborn
* **Environment:** Jupyter Notebook

## 📊 Analysis Summary (EDA)
### 1. 환자 인구 통계 (Demographics)
* **총 환자 수:** 100명
* **성별 분포:** (예: 남성 55%, 여성 45% - *본인 분석 결과 입력*)
* **평균 연령:** (예: 65.4세 - *본인 분석 결과 입력*)

### 2. 주요 분석 지표
* **평균 재원 기간 (Avg LOS):** (예: 4.5일)
* **사망률 (Mortality Rate):** (예: 12%)
* **가장 빈번한 진단명:** (예: Sepsis, Hypertension...)

*(이곳에는 분석한 그래프 이미지를 `![image](path/to/image.png)` 형태로 첨부하면 좋습니다)*

## 📂 Project Structure
```bash
├── data/               # 데이터 폴더 (gitignore 처리됨)
├── notebooks/          # 분석용 Jupyter Notebooks
│   ├── 01_data_loading.ipynb
│   ├── 02_eda_distribution.ipynb
│   └── 03_preprocessing.ipynb
├── src/                # 전처리 및 유틸리티 스크립트
├── README.md           # 프로젝트 설명
└── requirements.txt    # 필요 라이브러리 목록