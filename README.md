# Fake and real news dataset
## 뉴스 분류하기
프로젝트 기간: 2023/03/02(목) ~ 2023/03/06(월)  
<br/>
## 개요
뉴스를 분류하는 모델을 만드는 프로젝트입니다. 뉴스는 시사에 대한 정보입니다. 이것은 입 소문, 인쇄, 우편 시스템, 방송, 전자 통신 또는 관찰자나 사건 목격자의 증언같이 많은 매체를 통해 제공될 수 있습니다. 허나, 가짜 뉴스는 뉴스로 보이는 거짓 또는 오해의 소지가 있는 정보입니다. 그것은 종종 사람이나 기업의 평판을 손상 시키거나, 광고 수익을 통해 돈을 버는 것을 목표로 합니다. 미디어 학자인 놀런 히그돈은 가짜 뉴스를 "거짓 또는 오해의 소지가 있는 콘텐츠를 뉴스 형태로 음성, 서면, 인쇄, 전자 및 디지털 통신 등 다양한 형식으로 전달하는 것"으로 보다 광범위하게 정의했습니다. 한때 인쇄물에서 흔히 볼 수 있었던 가짜 뉴스의 보급률은 소셜 미디어, 특히 페이스북 뉴스 피드의 증가와 함께 증가했습니다. 가짜 뉴스는 진짜 뉴스의 영향을 줄일 수 있습니다. 그것은 또한 언론 보도에 대한 신뢰를 약화 시킬 수 있는 심각한 잠재력을 가지고 있습니다.  
진짜 뉴스와 가짜 뉴스를 분류하는 모델을 구축하면 가짜 뉴스의 영향을 줄임으로써 언론 보도에 대한 신뢰가 강화되므로 언론 회사에 매우 도움이 됩니다. 따라서, 뉴스가 진짜인지 가짜인지 분류하는 모델을 만들고자 하였습니다.  
<br/>
## 사용한 데이터셋
Fake and real news dataset: Classifying the news
- Clément Bisaillon
- https://www.kaggle.com/clmentbisaillon
- https://www.kaggle.com/datasets/clmentbisaillon/fake-and-real-news-dataset  

위 데이터셋은 "가짜" 뉴스로 간주되는 기사 목록과 "진짜" 뉴스로 간주되는 기사 목록 데이터를 가지고 있습니다.  
<br/>
## 프로젝트 목록
1. Basic Exploration
    - Read dataset
    - Some information
2. Data preprocessing
3. Exploratory Data Analysis
    - Check the balance between real and fake news
    - Count of News Articles by Subject
4. Machine Learning model
    - Logistic Regression
5. Conclusion  
<br/>

## 프로젝트 수행 과정
- target 변수를 설정하고, 진짜 및 가짜 뉴스 데이터 셋을 모두 결합하였습니다.
- 진짜 및 가짜 뉴스 데이터 셋은 모두 non-null 값을 가집니다. 따라서 결측값을 처리할 필요가 없었습니다.
- 보다 원활한 분석을 위해 불용어(Stopwords)를 제거하는 기능을 만들었습니다.
- 진짜 뉴스와 가짜 뉴스 분포 확인해보니 데이터 셋이 균형 잡힌 것처럼 보이기 때문에 균형 있게 만들기 위해 노력할 필요가 없습니다.
- 어떤 주제가 많나 확인해보니 PoliticalNews와 WorldNews가 데이터 셋에서 가장 많았습니다.
- Word Cloud를 사용하여 중요도나 사용 빈도를 직관적으로 파악할 수 있도록 시각화 해보았습니다.
- Logistic Regression을 사용하여 제목만 고려했을 때, 맥락만 고려했을 때, 제목과 맥락을 고려했을 때의 정확도와 Confusion Matrix를 살펴보았습니다.
<br/>

## 모델의 dataset에 대한 accuracy (소숫점 다섯 째 자리에서 반올림)
| Logistic Regression | accuracy |
|:----------------------------------------|:-------|
| 제목만 고려했을 때                       | 0.9475 |
| 맥락만 고려했을 때                       | 0.9953 |
| 제목과 맥락을 고려했을 때                | 0.9967 |
<br/>

## 최종 모델
Logistic Regression
- '제목과 맥락을 고려했을 때'에 대한 결과
    - accuracy: 약 0.9967
<br/>

## 결론
제목만으로 뉴스를 예측할 때 비교적 정확도가 낮았습니다. 뉴스기사 맥락을 고려했을 때는 정확도가 94%에서 99%로 급증하였습니다. 제목과 맥락을 모두 고려할 때, 우리는 가장 높은 정확도에 도달할 수 있었습니다. 이후 저는 더 나은 결과를 제공할 수 있는 추가 모델을 구현하기 위해 노력할 것입니다.
