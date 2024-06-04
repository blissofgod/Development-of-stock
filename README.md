세미프로젝트에서 최우수상을 받은 경험이 있습니다. 이때 진행한 프로젝트는 머신러닝 기술과 소셜 데이터를 활용한 주
가 어드바이저 개발이었습니다. 이 프로젝트는 SOXL 주가에 대해 강력 매수, 매수, 중립, 매도, 강력 매도의 5가지 추천을
제공했습니다.
저는 데이터 수집 및 전처리, 그리고 모델링 파트를 담당했습니다. 특히 레딧에서 셀레니움을 활용하여 데이터 크롤링하여
습니다. 추가로 인베스팅닷컴과 네이버 종목토론방에서 크롤링을 진행하여 약 16,000개의 데이터를 수집하였습니다.
전처리 과정에서 다양한 기법을 사용했습니다. 특히 성능이 가장 좋았던 방법은 IQR을 이용해 문서의 단어 수가 많은 경우
허깅페이스 모델을 이용해 문서 요약을 진행한 후 감성 분석을 하는 것이었습니다. 문서 요약을 통해 이상치를 식별하고,
감성 분석의 정확도를 높일 수 있었습니다.
두 번째 전처리는 데이터의 출처와 추출된 키워드를 원-핫 인코딩하는 것이었습니다. 세 번째 전처리는 주가의 변동량을
계산하는 것이었습니다. y 값으로 예측할 데이터에 대해서는 주가의 변동량을 구간별로 나누어 평균 주가 변동량의 150%
를 강력 매수로 예측했습니다. 과거와 현재 데이터의 변동량을 포함하니 성능이 상승했습니다.
네 번째 전처리는 헤드라인과 댓글에 대해 Word2Vec을 사용한 것이었고, 다섯 번째 전처리는 날짜 정보(며칠인지, 몇 월인
지, 무슨 요일인지, 일 년 중 몇 번째 주인지 등)를 포함하는 것이었습니다.
이렇게 전처리를 마친 후 모델링에는 9개의 모델을 사용했습니다: Logistic Regression, Random Forest Classifier, KNN, Support
Vector Classifier, Naive Bayes, Gradient Boosting, Decision Tree Classifier, Bagging, XGBClassifier. 이 중 성능이 가장 좋았던 Gradient
Boosting을 사용해 예측을 진행했으며, 목표로 했던 성능인 75%를 넘길 수 있었습니다.
