# 오토인코더와 OneClass SVM을 이용한 음향신호 이상치 탐지

['오토인코더와 OneClass SVM을 이용한 음향신호 이상치 탐지' 논문 보기](https://drive.google.com/file/d/1RHWmiwUu88hMRMgrtAOVEPF2x3jQRYXz/view?usp=sharing)

**요약**

본 연구에서는 세탁기 불량 탐지를 위하여 2,871개의 세탁기의 모터 음향신호를 바탕으로 딥러닝 기반의 Autoencoder와 머신러닝 기반의 OneClass SVM을 통하여 이상치 탐지를 하였다. Autoencoder의 경우 주파수 단위를 Mel 단위로 변환한 Mel-spectrum feature가 데이터로 사용 되었고, 옵티마이저 알고리즘으로는 Adam, 손실함수로는 Mean Squared Error가 사용되었다. 그리고 각 층의 활성함수는 ‘ReLu’를 이용하고 마지막 출력 층에는 Linear 활성함수를 사용하였다. Autoencoder는 학습한 데이터들의 재구성 손실 분포에 상위 5%는 불량인 Threshold를 설정하여 불량임을 판별하였다. 또한 OneClass SVM에서는 MFCC 알고리즘과 PCA를 사용하여 뽑은 feature가 데이터로 사용 되었고, 커널함수를 RBF로 두고 커널 감마계수와 오차 상한 계수를 변수로 두었다. 그 후 정상 Validation Data를 이용해 성능 확인을 했을 때 모두 정상이라고 잘 판별하는 시점의 파라미터를 가지는 모델로 불량 판별을 시행하였다. 학습 결과, 성능 측정에서 Oneclass SVM의 성능이 더 우수하다는 결론이 나왔다.

KeyWords: Anomaly Detection, Novel Detection, Convolutional Autiencoder, One-Class Support Verctor Machine, Audio Signal Feature Extraction, MFCCs, Machine Fault Diagnosis, Pattern Recognition

![image](https://user-images.githubusercontent.com/75656845/227200197-b74b3c25-bb65-4246-a0ab-35d63d15e6d8.png)
