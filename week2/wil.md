# GDG-deep_learning-W2-WIL
AI의 학습에 대해서 아주 추상적으로만 알고있었는데,  
'적절한 추론을 하도록 가중치를 조절하는 과정'이라고 말을 풀어놓고,  
추론이 뭔지, 가중치를 조절해서 최적화하는게 뭔지를 수식과 코드로 이해할 수 있었다.  
개인적으로 중요하거나, 헷갈렸다고 느낀것을 정리하면서 마무리하려고 한다.  
- 추론이 적절한 정도를 Cost Function으로서 cost를 낮추는 방향으로 학습을 진행하는것.  
- Gradient는 Cost가 가중치에 따라 어떻게 변하는지를 나타내고, Gradient Descent는 이를 이용해 가중치를 조금씩 조정하는 방법.  
- Learning rate가 너무 작으면 안정적이지만 느리고, 너무 크면 Cost가 발산..  
- MSE 공식에 맞춰 cost_func()를 구현하면서 예측값과 타겟값의 차이 -> 제곱 -> 평균 으로 구현.
- Keras에서도 (직접 실습한 grad() 함수가 없지만) 결국 Prediction -> Loss계산 -> Gradient 계산 -> Optimizer로 Weight update의 흐름으로 학습  
- TensorFlow의 자동미분은 Loss가 각 학습가능한 Weight에 따라 얼마나 변하는지 자동으로 계산해 gradient 구해줌