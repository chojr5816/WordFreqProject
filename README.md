# 📊 WordFreqWebDashboard

텍스트 데이터를 기반으로 단어 빈도수를 분석하고, 이를 막대그래프와 워드클라우드로 시각화해주는 웹 대시보드입니다.

다음(Daum) 영화 리뷰 데이터를 예시로 사용하여, 사용자가 자주 사용하는 단어를 한눈에 파악할 수 있도록 설계했습니다.

---

## 🖥️ 데모

> 실행 화면 스크린샷을 이곳에 추가해보세요. (예: `assets/demo.png`)

```
streamlit run WordFreqDashboard.py
```

---

## ✨ 주요 기능 (Highlights)

- **형태소 분석 기반 텍스트 처리**: KoNLPy(Okt)를 활용해 명사·동사·형용사만 추출
- **불용어(Stopwords) 제거**: 분석에 불필요한 조사·의미 없는 단어를 필터링하여 정확도 향상
- **상위 키워드 막대그래프**: 빈도수 상위 N개 단어를 시각화
- **실시간 워드클라우드 생성**: 사용자 입력 데이터를 기반으로 즉시 워드클라우드 렌더링

---

## 🛠️ 기술 스택 (Stack)

| 분류 | 기술 |
|---|---|
| Language | Python |
| Web Framework | Streamlit |
| 자연어 처리 | KoNLPy (Okt) |
| 시각화 | Matplotlib, WordCloud |
| 데이터 처리 | Pandas |

---

## 📁 프로젝트 구조

```
WordFreqProj/
├── WordFreqDashboard.py        # 메인 실행 파일 (Streamlit 앱)
├── mylib/
│   ├── myTextAnalyzer.py       # 텍스트 로드 및 형태소 분석, 빈도수 계산
│   └── MyStreamlitVisualizer.py # 막대그래프 / 워드클라우드 시각화
├── data/
│   └── daum_movie_review.csv   # 분석 대상 데이터 (다음 영화 리뷰)
├── requirements.txt
└── README.md
```

---

## 🚀 설치 및 실행 방법

### 1. 저장소 클론
```bash
git clone https://github.com/yourusername/WordFreqProj.git
cd WordFreqProj
```

### 2. 가상환경 생성 (선택 사항이지만 권장)
```bash
python -m venv venv
venv\Scripts\activate   # Windows
# source venv/bin/activate   # Mac/Linux
```

### 3. 필요한 패키지 설치
```bash
pip install -r requirements.txt
```

> ⚠️ KoNLPy는 Java(JDK) 설치가 필요합니다. [KoNLPy 공식 설치 가이드](https://konlpy.org/ko/latest/install/)를 참고해주세요.

### 4. 앱 실행
```bash
streamlit run WordFreqDashboard.py
```

브라우저에서 `http://localhost:8501` 접속 시 대시보드를 확인할 수 있습니다.

---
