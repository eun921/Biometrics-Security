# Biometrics-Security
## 2021-1 생체인증보안</br>

아래 항목들에 대해 다음 과정을 수행했다. </br>
제공된 트레이닝 데이터셋을 이용하여 아래 항목을 인식하는 인공지능 모델을 구현하고, 구현된 모델을 이용하여 테스트 데이터셋에 대해 분류를 진행한다.</br>

1. 지문
 - CNN모델 사용
 - ![image](https://user-images.githubusercontent.com/62167576/119311075-93cc4780-bcab-11eb-95f9-34b887fbba15.png)</br>
2. 얼굴
 - CNN모델 사용
 - ![image](https://user-images.githubusercontent.com/62167576/119311140-a6df1780-bcab-11eb-9e9b-0b886d95d377.png)</br>
 - 1차 제출 이후 Batch Normalization Layer 제거하고 batch size를 변경해 Test accuracy 개선함.</br>
3. 홍채
 - ResNet50 사용
 - ![image](https://user-images.githubusercontent.com/62167576/127138075-47afdbc3-94bf-4dec-be8e-04af5132cd2b.png)</br>
 - 1차 제출 시에는 CNN 계층 3개를 쌓아서 사용했으나 2차에는 Pretrained model인 ResNet50을 사용. Test accuracy 개선했음.</br>
4. 모달
 - model1은 모델 1개 사용한 것. 홍채와 얼굴 데이터를 합쳐 하나의 데이터로 만들고 그것을 모델의 input으로 넣음.</br>
 - DenseNet121 사용
 - model2는 홍채와 얼굴 각각에 대한 모델을 생성해 학습시키고, 두 결과값을 비교해 더 큰 것을 최종 결과로 선택함. </br>
 - 홍채, 얼굴 모델 모두 DenseNet121 사용
