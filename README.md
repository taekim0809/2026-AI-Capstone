# 2026-AI-Capstone
# 2026 AI Data Convergence Capstone

## 강수량 기반 전국 침수 위험지역 예측 및 시각화

### 📌 프로젝트 소개

강수량과 지역의 지형·환경적 특성을 활용하여 **전국의 침수 발생 위험을 예측하고 지도 형태로 시각화**하는 프로젝트이다.

전국을 일정한 크기의 격자로 나누고, 각 격자에 강수량, 고도, 경사도, 하천과의 거리, 토지피복 등의 데이터를 결합하여 침수 발생 여부를 예측한다.

### 🎯 목표

* 강수량 및 공간 데이터를 활용한 침수 위험 분석
* 지역별 지형·환경 특성을 반영한 침수 예측
* 격자 단위 침수 위험지역 시각화
* 실제 침수흔적도와 예측 결과 비교

### 🗂️ 주요 데이터

| 데이터         | 활용           |
| ----------- | ------------ |
| 침수흔적도       | 실제 침수 발생 여부  |
| AWS         | 강수량          |
| DEM         | 고도·경사도       |
| 하천 공간정보     | 하천과의 거리      |
| 토지피복/불투수면   | 불투수면 비율      |
| 전국 격자       | 공간 데이터 통합 기준 |
| 도시침수지도(WMS) | 추가 비교·분석     |

### 🔄 프로젝트 흐름

```text
데이터 수집
    ↓
공간 데이터 전처리
    ↓
전국 격자 단위 데이터 통합
    ↓
침수 여부 생성
    ↓
EDA 및 특성 분석
    ↓
침수 예측 모델 학습
    ↓
모델 평가
    ↓
침수 위험지역 시각화
```

### 🤖 모델

침수 발생 여부를 예측하는 **분류(Classification)** 문제로 접근한다.

* Random Forest
* XGBoost
* 기타 모델

※ 최종 모델은 실험 결과에 따라 결정한다.

### 🛠️ 개발 환경

* Python
* Google Colab
* GitHub

주요 라이브러리: `pandas`, `numpy`, `geopandas`, `rasterio`, `scikit-learn`, `matplotlib` 등

### 📁 Repository Structure

```text
2026-ai-capstone-flood/
│
├── README.md
├── data/
│   └── README.md
├── notebooks/
│   ├── 01_data_preprocessing.ipynb
│   ├── 02_EDA.ipynb
│   ├── 03_model.ipynb
│   └── 04_visualization.ipynb
├── src/
└── results/
```

### 👥 협업

* **GitHub**: 코드 및 파일 관리
* **Google Colab**: 데이터 전처리 및 모델 개발
* **Notion**: 프로젝트 문서 및 진행 상황 관리

### 📝 Commit Convention

| Prefix       | 용도           |
| ------------ | ------------ |
| `feat`       | 새로운 기능/코드 추가 |
| `fix`        | 오류 수정        |
| `data`       | 데이터 추가 및 전처리 |
| `docs`       | 문서 수정        |
| `refactor`   | 코드 구조 수정     |
| `experiment` | 모델 실험        |

#### Commit 예시

```text
feat: 침수 예측 모델 추가
data: AWS 강수량 전처리
experiment: Random Forest 학습 결과 추가
fix: 격자 공간연산 오류 수정
docs: README 수정
```

### 📚 Data Sources

공공데이터 및 국가 공간정보를 활용한다.

* 기상청 AWS 관측자료
* 침수흔적도
* DEM
* 하천 공간정보
* 토지피복/불투수면
* 전국 격자
* 도시침수지도

※ 데이터별 상세 출처와 다운로드 방법은 `data/README.md`에 정리한다.
