# 04-2 확률적 경사 하강법
## 확률적 경사 하강법
* 앞서 훈련한 모델을 버리지 않고 새로운 데이터에 대해서만 조금씩 더 훈련하는 '점진적 학습'을 기반한 알고리즘
* 훈련세트에서 랜덤하게 하나의 샘플을 고르는 방법
* 에포크: 훈련세트를 한번 모두 사용하는 과정
* 여러가지 하강법
  * 미니배치 경사 하강법
  * 배치 경사 하강법
 
## 손실함수
* 알고리즘이 엉터리인지 측정하는 기준
* 미분 가능(연속적) -> 0~1 사이의 확률을 출력하는 로지스틱 회귀(이진분류) 사용

## 로지스틱 손실함수
* 이진분류에 사용(다중분류는 크로스엔트로피 손실함수)
* 로지스틱 손실함수를 통해 로지스틱 회귀를 모델링

## SGDClassifier
* 확률적 경사 하강법 제공(분류용 클래스)
## partial_fit()
* 호출시마다 1에포크씩 훈련하여 점진적 학습이 가능함
* 모델 생성 후, fit()을 사용하지 않고 위의 함수에 훈련 세트의 전체 클래스의 레이블을 전달하여 사용
## 에포크 과대/과소 적합
* 과대적합 되기 전에 훈련 종료(조기 종료)
