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
- 데이터 불러오기 및 레이블 추가: 데이터를 불러와 진짜 뉴스와 가짜 뉴스를 구분하기 위한 레이블을 추가하고, 두 데이터셋을 결합하였습니다. 데이터셋에는 결측값이 없었습니다.
- 데이터 전처리: NLTK를 사용하여 불용어를 제거하고 텍스트 데이터를 토큰화하고 소문자로 변환하며 특수 문자를 제거하는 전처리 작업을 수행하였습니다. TF-IDF 벡터화를 통해 텍스트 데이터를 수치화하였습니다.
- 데이터 분석: 진짜 뉴스와 가짜 뉴스의 분포를 확인하고 주제별 뉴스 카운트를 시각화하여 데이터를 분석한 결과 데이터 셋이 균형 잡힌 것처럼 보이기 때문에 균형 있게 만들기 위해 노력할 필요가 없었고, PoliticalNews와 WorldNews가 데이터 셋에서 가장 많은 지배적인 카운트를 보유하고 있습니다.
- 머신러닝 모델 선택 및 학습: 로지스틱 회귀 모델을 선택하고 학습 데이터와 테스트 데이터로 데이터를 분할하였습니다.
- 모델 평가: 모델의 성능을 평가하고 정확도, 혼동 행렬, Precision, Recall, F1-score 등의 평가 지표를 계산하였습니다. 모델은 높은 성능을 보였으며, 정확도는 98.82%였습니다.
- 교차 검증: 5-폴드 교차 검증을 수행하여 모델의 일반화 능력을 평가하였으며, 평균 정확도는 98.65%였습니다.
- 결론: 프로젝트는 높은 성능의 모델을 개발하여 가짜 뉴스와 진짜 뉴스를 신뢰성 있게 분류할 수 있음을 입증하였으며, 정보 신뢰성 향상과 가짜 뉴스의 확산 억제에 기여할 것으로 기대됩니다.
<br/>

## 모델의 가짜 뉴스 (0)에 대한 Accuracy, Precision, Recall, F1-score (소숫점 넷 째 자리에서 반올림)
|| Accuracy | Precision | Recall | F1-score |
|:------------------|:-------|:-------|:-------|:-------|
|Logistic Regression| 0.9881 | 0.9829 | 0.9928 | 0.9878 |
<br/>

## 최종 모델
Logistic Regression
- accuracy: 약 0.9881
<br/>

## 결론
이 프로젝트는 가짜 뉴스와 진짜 뉴스를 분류하는 작업을 통해 매우 뛰어난 성과를 달성했습니다. 최종 모델의 정확도는 98.81%로, 가짜 뉴스와 진짜 뉴스를 높은 신뢰도로 분류할 수 있음을 입증했습니다.

Confusion Matrix를 살펴보면, 가짜 뉴스와 진짜 뉴스에 대한 예측 결과가 매우 밸런스 있음을 확인할 수 있습니다. 가짜 뉴스에 대한 정확한 예측 수는 4584건이며, 진짜 뉴스에 대한 정확한 예측 수는 4298건입니다. 또한, 거짓 긍정과 거짓 부정의 수가 상대적으로 매우 낮음을 확인할 수 있습니다.

Classification Report에서는 가짜 뉴스와 진짜 뉴스에 대한 Precision, Recall, F1-score, 그리고 Support 값을 상세히 보여줍니다. 가짜 뉴스와 진짜 뉴스에 대한 모든 메트릭이 높은 값을 기록하고 있으며, 모델의 품질이 뛰어나다는 것을 명확하게 나타냅니다.

이러한 결과를 종합적으로 고려할 때, 이 프로젝트는 정보 신뢰성을 향상시키고 가짜 뉴스의 확산을 억제하는 데 큰 기여를 할 것으로 기대됩니다. 이 모델은 현실 세계에서 신뢰할 수 있는 뉴스 판별을 지원하고, 정보 환경의 개선에 기여할 것입니다.

더불어, 향후 연구에서는 더 많은 데이터와 향상된 알고리즘을 활용하여 모델의 성능을 더욱 향상시킬 예정입니다. 이러한 노력을 통해 뉴스 신뢰성과 정보 확산의 문제에 대한 해결책을 지속적으로 발전시켜 나갈 것입니다.
