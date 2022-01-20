# Traffic_sign_recognition
### 1. Test loss: 0.946179	Test accruacy: 85.463% 


<img src="https://github.com/syoung7388/Traffic_sign_recognition/blob/main/modeling.png" width="70%" height="50%">



#### * Action Function - ReLu [max(0, x)]
#### * Loss Function - Cross Entropy Loss
#### * Optimizer - SGD


### 2. Test loss: 0.601990	Test accruacy: 87.070% 

<img src="https://github.com/syoung7388/Traffic_sign_recognition/blob/main/Gray.PNG" width="70%" height="50%">

회색조란 컬러이미지에서 광도만 표현한 색 채널이다. 밝은 부위는 흰색, 어두운 부위는 검은색으로 표현되는 색채널이다. 
RGB는 255X255X255란 계산을 해야한다. 하지만, Grayscale 은 1차원이므로 연산량이 대폭 감소하게 되는 장점이 있다.  그럼 왜 자동차 표지판에서 회색조를 사용해야 할까 ? 사실, 자동차 표지판은 색깔 상관 없이 구분이 가능하다. 그래서 연산량을 대폭 감소할 수 있는 Grayscale을 쓰는게 좋다. 


