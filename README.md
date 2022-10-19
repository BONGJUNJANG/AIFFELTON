<h1 align="center"> <br>딥러닝을 활용한 비트코인 추세예측📈</h1>
<h3 align="center"> <br>💰 Bit주세요 💰</h3>
<h5 align="center"> Fn Guide 기업과제
<h5 align="center"> 딥러닝 모델을 활용하여 비트코인의 추세를 예측, 실제로 사용할 수 있는 투자전략 구축
</h5>
<br>

> #### [발표 자료]()

> #### [팀 노션 페이지](https://roan-prince-424.notion.site/Bit-572682b84cf4461eadffd8fcec61f14f)
 
<br>

## 💸  Goal
* 가상화폐 시장이 지속적으로 성장하는 상황에서 투자자의 편견 등으로 매매 타이밍 결정에 어려움을 겪는 문제점 발생
* 머신러닝 및 딥러닝 모델을 활용하여 가상화폐(이더리움) 가격의 상승 및 하락 여부 판단
<br>

 
## 💸  Outline
1. Trend 또는 Momentum 을 정의

2. 정의된 Trend / Momentum 을 가장 잘 파악할 수 있는 Feature추출

3. ML 모델을 선정, 학습

4. ML 모델의 정확도, 예측력을 검증

5. ML 모델의 신뢰도에 따라 Betting Size를 결정하여 투자전략 구축

6. Back Testing

<br>
 
 
<h2> 💸  Process  </h2>
 
### 1. Trend 또는 Momentum 을 정의
* 이더리움 1년치 분봉 데이터를 Trend Scanning 기법을 사용하여 상승, 하락, 보합으로 라벨링

| | 내용  |
| ------- | ------ | 
| Data | Upbit 이더리움 1분봉 데이터 |
| 데이터 스무딩 | centered MA |
| labeling method | Trend scanning |

</br>  
  
  
### 2. 정의된 Trend / Momentum 을 가장 잘 파악할 수 있는 Feature추출


| | Features  |
| ------- | ------ | 
| 가격변수 | MA, ROC, 모멘텀, SHochastic osillator, RSI, MACD, 볼린저 밴드 , ADX/MDI, 가격 및 거래량 비율 지표 |
| 수요공급지표 | 비트코인 종가,달러인덱스,비트코인 도미넌스, S&P 500, 김치프리미엄, 디파이 예치금 |
| 심리변수 | 뉴스기사 빈도수, 네이버 트랜드 |
| 유동성 지표 | kyle lambda, Amihud lambda, Hasbrouck lambda |

</br>  
  
### 3. ML 및 DL 모델을 선정, 학습
| 머신러닝 | 딥러닝  |
| ------- | ------ | 
| LGBM |LSTM  |
| RF |1DCNN |
| SVM |1DCNN+LSTM  |
| logistic regression |BiLSTM  |
 
| Ensamble  |
| ----------- | 
|1DCNN + BiLSTM  |
|RF + BiLSTM|
  
</br>  

### 4. ML 및 DL 모델의 정확도, 예측력을 검증

* Soft Voting(Random Forest + BiLSTM)을 통해 0.4466(f1-score) 성능 도출

| 머신러닝 | F1-score |
| ------- | ------ | 
| LGBM | 0.3860 |
| RF | 0.4037 |
| SVM | 0.3217 |
  
| 딥러닝 | Micro F1-score  |
| ------- | ------ | 
| LSTM| 0.3515 |
| 1D-CNN | 0.3569 |
| 1DCNN+LSTM |0.3424  |
| BiLSTM  | 0.3734 |
| 1DCNN+BiLSTM Ensambel  | 0.3594 |
| RF+BiLSTM Ensambel  | 0.4466 |
 
 
</br>  
 
 
### 5. ML 모델의 신뢰도에 따라 Betting Size를 결정하여 투자전략 구축
|  |  |
| ------- | ------ | 
| 2% Rule |  |

  
### 6. Back Testing
 
<br>
 


<h2> 💸  Further  </h2>
<br>
 

## 💸 Team
### 💰Bit주세요 
| Tesk | 담당자 | 기타 |
| -------  | ------ | ------|
| 데이터 EDA & 전처리 | 이동현, 김은경 | Data smoothing 및 Labeling  |
| Feature engineering | 김덕우, 장봉준 | 주가 추세에 영향을 미치는 Feature 선정 및 Feature별 중요도 분석 |
| Modeling | 김동연, 조경모 | ML및 DL모델을 이용한 추세 학습|
* 김덕우 : 건설 관련 업종에서 일을하다가 프로그래머가 한번 되어보고 싶어서 아이펠에 참여했습니다. 멋진 가상화폐 추세 분석기를 만들어서 우리 부자 됩시다! 
* 김동연 : 안녕하세요. 김동연이라고 합니다. 머신러닝과 금융분야 비전공자이지만 열심히하겠습니다. 저의 목표는 이번 아이펠 교육과정과 프로젝트를 통해 관련해서 portfolio 작성하고 머신러닝이 제 전문분야에서 synergy를 발휘하여 제 Career를 향상시키는 것입니다.
* 김은경 : 자동매매 프로그램에 관심이 있습니다. 프로젝트 기간동안 즐거운 시간 되었으면 좋겠습니다 !! 
* 이동현 : 프로젝트 주제에 흥미가 있어 참여하였습니다. 끝까지 잘 마무리되어 모두가 만족할 수 있는 결과물이 나오면 좋을 것 같습니다. 
* 장봉준 : 금융데이터를 다뤄보고 싶어 프로젝트에 참여하게 되었습니다. 열심히 많이 배워가겠습니다! 
* 조경모 : 딥러닝을 활용한 퀀트 투자에 관심이 있습니다. 한달동안 다들 화이팅!!! 
