# Predict survival on the Titanic with ML(Kaggle competition)
https://www.kaggle.com/c/titanic<br>
 
 ## Abstarct
  1912년 4월 15일, 타이타닉의 항해 도중 빙산과 충돌한 후 침몰하였고, 이로 인해 2224명의 승객과 승무원 중 1502명이 사망하였습니다. 전 어떤 부류의 사람들이 생존할 가능성이 높았었는지에 대해 분석을 하고, 머신러닝 모델을 만든 뒤 승선한 사람들의 생존유무를 예측하여야 합니다. 891개의 train data로 학습하여 418개의 test data set의 생존유무를 예측합니다. data field는 총 11개, 예측해야하는 label은 생존유무, 즉 1개입니다. <br>
  데이터 분석, 마이닝, 전처리부터 모델 선택, 학습 및 예측까지 모든 코드를 담고 있습니다. 코드는 전부 python으로 작성되었습니다.
 
 ## Data analysis, mining, preprocessing
 - 데이터 시각화 및 분석
 - null value 확인 및 fill
 - One-Hot-Encoding을 통한 cateorical feature -> dummy variable

해당 데이터 셋은 결측치가 상당부분 존재합니다. 이 결측치에 대하여 어떻게 채워나갈 것인지가 가장 큰 문제이고, 이러한 문제에 대한 개인적인 생각과 해답을 작성하였습니다.
 
## Modeling
  학습에 사용된 모델은 아래와 같습니다.
 1. GradientBoosting
 2. Randomforest
 3. XGBoost
 4. LightGBM
 5. MLP Classifier
 6. MLP(hidden layer 2개, tensorflow)
 
모델의 정의, 학습, 검증을 진행하고 ensemble 기법을 사용하여 최종적으로 train 하고 5가지 model을 선정해 결과를 도출했습니다. 중간의 검증과정에서는 단순 데이터 분리를 하여 검증을 해보고, k-fold cross validation을 사용하여 검증, 가장 cost가 적은 모델을 선정했습니다.<br>
## Summary
데이터의 양이 굉장히 적어 예측이 쉽지 않은 문제였습니다. 기존에 존재하는 데이터를 활용하여 특정 결측치를 채워넣거나, 특정 field를 추가로 생성하여 accuracy를 높였고, 다양한 model을 실습해보고 공부할 수 있습니다.
