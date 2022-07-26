# Resnet-in-Pytorch

ResNet
=====

Resnet은 Deep Residual Learning for Image Recognition 잔차를 학습한다 하여 ResNet이라는 명칭이 붙음

기존의 CNN 방식과는 다른 접근 방식으로 Accuracy를 높임.

VGG Net같은 경우에는 기존의 모델에서 3x3 Convolution layer와 Maxpooling을 활용하여 층일 깊게 쌓으면서 Model의 Accuracy를 높임.

층이 깊어질수록 성능이 증가하긴 하나 어느정도 수준에 다다르면 오히려 과적합이 발생하며 Update가 안되는 상황이 발상하며, Gradient Vanishing 문제가 발생.

ResNet은 이러한 여러 문제점을 보안하기 위하여 예측하려는 output H(x) 보다는 F(x)+x의 형태로 기존의 분류되기 전의 데이터까지 함께 학습을 진행하여 성능을 높임

즉 잔여 블록 Residual Block 활용 하여서 학습을 진행함

기존 학습 방식: x->weight layer->activation->weight layer-> H(x) -> activation = plain layer 이러한 학습 형태를

ResNet 학습 방식: x->weight layer -> activation -> weight layer-> F(x)+x(앞서 학습된 정보 그대로 가져오고 F(x)=잔여정보) -> activation = Residual Block 


ResNet 구조
======

![image](https://user-images.githubusercontent.com/104436260/180899320-a62503ce-6a0e-478d-85b5-373174b65a66.png)

Conv1 define
=====

![image](https://user-images.githubusercontent.com/104436260/180921724-833ea279-7464-4af4-8c4a-ae7f8f614ca5.png)

Conv1 define 


Conv1x1, Conv3x3 define
========

![image](https://user-images.githubusercontent.com/104436260/180930239-486ac59f-eefe-445d-a8d1-5eadcb0fcce8.png)
