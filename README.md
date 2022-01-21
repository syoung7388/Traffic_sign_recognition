# Traffic_sign_recognition
### 1. Test loss: 0.946179	Test accruacy: 85.463% 


<img src="https://github.com/syoung7388/Traffic_sign_recognition/blob/main/modeling.png" width="70%" height="50%">



#### * Action Function - ReLu [max(0, x)]
#### * Loss Function - Cross Entropy Loss
#### * Optimizer - SGD


### 2. Grayscale (Test loss: 0.601990	Test accruacy: 87.070% )

<img src="https://github.com/syoung7388/Traffic_sign_recognition/blob/main/Gray.PNG" width="70%" height="50%">

회색조란 컬러이미지에서 광도만 표현한 색 채널이다. 밝은 부위는 흰색, 어두운 부위는 검은색으로 표현되는 색채널이다. 
RGB는 255X255X255란 계산을 해야한다. 하지만, Grayscale 은 1차원이므로 연산량이 대폭 감소하게 되는 장점이 있다.  그럼 왜 자동차 표지판에서 회색조를 사용해야 할까 ? 사실, 자동차 표지판은 색깔 상관 없이 구분이 가능하다. 그래서 연산량을 대폭 감소할 수 있는 Grayscale을 쓰는게 좋다. 


### 3. Flipping (Test loss:0.558004	Test accruacy: 88.424% )

수평으로 뒤집기, 수직으로 뒤집기, 혹은 둘다 뒤집어서 training data를 늘려서 학습률을 높여준다. 


### 4. Augmentation (Test loss: 0.598987	Test accruacy: 88.250%)

![image](https://user-images.githubusercontent.com/79610047/150470745-964fe9b6-1aa3-48a6-a8e4-ad687911609d.png)
![image](https://user-images.githubusercontent.com/79610047/150470702-9b45b415-0424-4742-b2d0-626369f1b726.png)


데이터 수를 20000개로 늘려서 고르게 분포하게 해준다.


### 5. Model - BatchNorm2d  (Test loss: 0.118326	Test accruacy: 96.619%)
학습과정을 안전하게 해주고 속도를 빠르게 해준다. 
?????   

### 6. STN(Test loss: 0.089112	Test accruacy: 97.443%)

이미지의 관심 영역을 잘라내거나, 크기를 조정하거나, 방향을 수정하는 것이다. 이러한 회전, 크기 조정 등의 일반적인 아핀(Affine) 변환된 입력에 대해 결과의 변동이 크기 때문에, STN은 이를 극복하는데 매우 유용한 메커니즘이다. STN이 가진 장점중 하나는 아주 작은 수정만으로 기존에 사용하던 CNN에 간단하게 연결 시킬 수 있다는 것이다. 




