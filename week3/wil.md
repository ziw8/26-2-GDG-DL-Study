CNN을 공부했다. Dense Layer와 CNN의 차이를 단순히 1차원과 2차원 데이터 차이 인줄 알았는데,  
그 차이가 왜 생기는지(작은 영역별로 계산하는 CNN), 그 차이 때문에 CNN이 어떤 특징을 가지는지 배웠다.  
Pooling이 필터를 적용하는 과정인 줄 알았다. Convolution과 Pooling 모두 작은 영역을 대상으로 계산하는 것이라서 헷갈렸다.
강의록 그림에서 Convolution을 왜 여러 번 반복하는지도 궁금했다.
처음에는 Kernel Size나 Stride를 다르게 설정하면서 반복하는 것인가? 생각했는데, 그게아니고..  
앞에서 추출한 Feature Map을 다음 Convolution의 입력으로 사용하면서 더 복잡한 특징을 학습하는 것이었다.(강의에서 해주신것 같은데 3주만에 해서 까먹은듯)  

헷갈리거나 남겨둔것..  
- Flatten으로 이미지를 펼치면 픽셀 간의 위치 관계를 직접 활용하기 어려워지고, CNN은 이미지의 공간적 구조를 유지하면서 특징을 추출한다는 점.  
- Convolution은 작은 영역에 필터(Kernel)를 적용해 특징을 추출하는 과정. 필터를 이동시키며 계산한 결과가 Feature Map이 됨.  
- Feature Map 사이즈를 공식으로도 계산할 수 있고, 아니면 잘 생각해보면 공식을 바로 유도해서 쓸 수도 있을것 같음.  
- Pooling은 추출된 특징을 요약하고 Feature Map의 크기를 줄이는 과정. Max Pooling은 영역에서 최댓값을 선택하는 방식.  
- Stride는 필터가 이동하는 간격. Padding은 Convolution 과정에서 Feature Map의 크기가 줄어드는 것을 방지하거나 조절하는 방법.  
- Convolution을 여러 번 반복하는 이유는 앞에서 추출한 특징들을 다시 조합해 더 복잡한 특징을 학습하기 위해서.  
- Feature Extraction은 Convolution과 Pooling 등을 거치며 특징을 추출하는 과정. 이후 Flatten과 Dense 등을 통해 Classification을 진행.  