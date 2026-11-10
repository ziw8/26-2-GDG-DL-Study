week5-wil
지난주차까지 주로 다루었던 이미지 데이터와 달리, 데이터의 순서가 중요한 순차 데이터(Sequential Data)의 종류와 특징을 공부하고,  
이를 처리하기 위한 NLP(자연어 처리) 기술이 어떻게 발전해왔는지 배웠다.   
순서와 문맥을 처리하기 위해 이전 정보를 활용하는 구조인 RNN이 등장했다. 현재 시점의 입력과 이전 시점의 Hidden State를 이용해 새로운 Hidden State를 계산하고,  
이를 다음 시점에 전달하여 순차 데이터의 문맥을 학습하는 신경망이었다.  
하지만 RNN은 역전파 과정에서 먼 과거로 전달되는 기울기가 점점 작아지는 기울기 소실(Vanishing Gradient) 문제가 발생할 수 있었다.  
이로 인해 오래전 입력과 현재 출력 사이의 관계를 학습하기 어려웠고, 이를 개선하기 위해 LSTM이 등장했다.  
LSTM은 Cell State와 Gate를 활용하여 필요한 정보를 오래 유지하고 불필요한 정보를 제거하도록 학습한다.  
이후 등장한 GRU는 LSTM과 비슷한 목적을 가지지만, 별도의 Cell State 없이 Update Gate와 Reset Gate를 이용한다.  
RNN 계열 모델을 이용한 Seq2Seq 구조에서는 Encoder가 입력 문장을 읽고, 최종 Hidden State를 Context Vector로 전달하여 Decoder가 출력 문장을 생성하도록 했다.  
하지만 입력 문장이 길어져도 Context Vector의 크기는 일정했기 때문에, 많은 정보를 하나의 벡터에 압축해야 하는 한계가 있었다.  
이를 개선하기 위해 등장한 것이 Attention이다. Decoder가 Encoder의 마지막 Hidden State에만 의존하는 대신, 각 시점의 Hidden State를 다시 참고할 수 있도록 했다.