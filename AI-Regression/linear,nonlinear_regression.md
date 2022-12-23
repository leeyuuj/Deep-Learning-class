# 선형 회귀 (Linear Regression)



![Normdist_regression](https://user-images.githubusercontent.com/109254161/183783366-fcead578-21c8-4d4c-9586-4996b2fc9a57.png)

## 정의 

$y$와 1개 이상의 $x$의 선형 상관 관계를 모델링하는 회귀분석 기법 [출처 : wikipedia]

### 단순 선형 회귀 분석 (Simple Linear Regression Analysis)
>하나의 $x$ 값으로 $y$ 값을 설명할 수 있는 경우를 단순 선형 회귀(simple linear regression)라고 한다.

> $y = \beta_0 + \beta_1x $
* Parameter : $\beta_1$ (weight)
* Bias : $\beta_0$

![스크린샷_2017-11-15_오전_12 33 47](https://user-images.githubusercontent.com/109254161/183783423-9aff100c-6140-4b5a-8e0d-3ba63fce0aab.png)

[출처](https://m.blog.naver.com/PostView.naver?isHttpsRedirect=true&blogId=anthouse28&logNo=221149064073)

"데이터를 가장 잘 설명하는"이라는 의미 : "실제값과 예측차이가 작은"
> 최적의 회귀모델을 만든다 => 잔차(오차값)합이 최소가 되는 모델을 만든다</br>
> 선형 회귀 모델은 최적의 $w$와 $b$를 찾기 위해 비용함수 MSE를 활용하여 경사하강법을 수행한다.

## 최소제곱법 (Least squares)
* 실제 $y$ 값과 예측 $y$값의 차이, 즉 데이터의 잔차 합이 최소가 되는 모델
* 잔차의 제곱합(RSS; Residual Sum of Squares)을 최소화하는 parameter 찾기

$RSS = \displaystyle\sum_{i=0}^n e_i^2 = e_1^2 + e_2^2 + \dots + e_n^2$

#### 오차항에 대한 가정
오차항은 모수이므로 우리는 그 값을 알수없다.</br>
때문에 잔차항 e로 가설을 검정하여, 다음의 가설이 성립하면 회귀 분석을 시행한다.

1. 오차들의 평균 = 0
2. 등분산성 : 오차들은 같은 정도로 퍼져있어야한다.
3. 독립성 : 오차항끼리는 독립
4. 정규성 : 오차들은 평균 0을 중심으로 정규분포를 이룬다.

### 다중 선형 회귀 (Multiple Linear Regression)

> 2개 이상의 $x_1, x_2, x_3$ 등의 값을 사용하는 경우를 다중 선형 회귀(multiple linear regression)라고 한다.</br>

$y = \beta_1x_1 + \beta_2x_2 + ... + \beta_nx_n + b$

현실에서 일어나는 대부분의 일은 여러 개의 독립 변수를 가질 수밖에 없으므로 다중 선형 회귀가 많이 사용되며, 일반적으로 선형 회귀는 다중 선형 회귀를 나타낸다.

## 선형 회귀의 장점
1. 복잡한 모델을 쉬운 계산들로 분해할 수 있다.

2. 모델의 해석이 쉽고 직관적이다.

3. 복잡한 패턴을 요구하지 않는 데이터에서 견고한 추정이 가능하다.


## 가설 함수 
* 데이터 속에서 가장 적합한 최적선을 찾기위해 다양한 값들을 넣어서 시도해봐야하는데, 이렇게 만들어진 함수를 가설함수라고 한다.

$h_\theta(x)= \theta_0+\theta_1x_1+\theta_2x_2+...$

선형회귀에서는 적절한 $\theta$값을 찾으면 된다.

### 평균 제곱 오차(MSE)

평균 제곱 오차는 각 데이터와 가설 함수 사이에 나타나는 오차를 다 구하여 오차값들을 모두 제곱한다. </br>
(제곱하는 이유는 데이터가 음수일 수 있기 때문에, 이들을 양수로 통일하기 위해서, 오차를 더 부각시키기 위해)

$\displaystyle\frac{1} {m} \sum_{i=1}^{m}(\hat{y^i}-y^i)^2$

### 비용 함수
> 가설함수를 평가하기 위한 함수
> 손실 함수의 결과가 작을수록 가설함수의 손실이 적다는 것이기에 좋은 가설 함수라고 평가할수 있다. 

$J(\theta)= \displaystyle\frac{1}{2m} \sum_{i=1}^{m}(\hat{y^i}-y^i)^2$

# 비선형 회귀 (Nonlinear Regression)

> 어떤 형태로 위의 식들과 같이 변환해도 $coefficient$(계수)를 선형식으로 표현하기 어려운 비선형 관계를 나타내는 회귀 분석

> 대표적 활성화 함수 : 시그모이드 함수, 탄젠트 함수, ReLU 함수
 * 출력을 0과 1로 이진값만 반환

$\sigma=\displaystyle\frac{1}{1+e^{-x}}$

![nonlinear](https://user-images.githubusercontent.com/109254161/183783465-b88687d1-b290-4dac-a919-9d7281309bb0.jpeg)

[출처](https://reniew.github.io/12/)

* 일정 구간은 선형성을 띄지만 일정구간은 선형적 성격을 띄지 않는다.

## 장점 및 특징

* 선형모델보다 정확하고 유연성을 지니고있어 둘 이상의 변수간의 복잡한 패턴을 갖는 데이터도 예측이 가능하고 다양한 곡선을 수용할수있다.</br>
* 충분히 많은 데이터를 갖고 있어서 variance error를 충분히 줄일수 있고 예측 자체가 목적이면 사용할만한 도구이다.
* 신경 회로망 가운데 가장 많이 사용되는 multi-layer perceptron(다층 퍼셉트론)


## 탄젠트 함수

$tanh(x) = \sigma(2x)-1$ </br>
$tanh(x) = \displaystyle\frac {e^x-e^(-x)}{e^x+e^(-x)}$

![tanh](https://user-images.githubusercontent.com/109254161/183783501-ed4532f9-bcc7-4637-92c8-74dfb27479cc.png)

[출처](https://reniew.github.io/12/)

### 탄젠트 함수의 단점

* 미분함수에 대해 일정값 이상 커질시 미분값이 소실되는 기울기 소실 문제는 여전히 남아있다.

## ReLU 함수 (Rectified Linear Unit)

$f(x) = max(0, x) $


![ReLU](https://user-images.githubusercontent.com/109254161/183783535-f3e4136d-fc57-45fc-8403-a003df1b1761.png)


[출처](https://reniew.github.io/12/)


### ReLU함수의 특징
* $x > 0$ 이면 기울기가 1인 직선이고, $x < 0$ 이면 함수값이 $0$이된다.
* sigmoid, tanh 함수와 비교시 학습이 훨씬 빨라진다.
* 연산 비용이 크지않고, 구현이 매우 간단하다.
* $x < 0$ 인 값들에 대해서는 기울기가 $0$이기 때문에 뉴런이 죽을 수 있는 단점이 존재한다.

# 선형 회귀와 비선형 회귀의 차이점 


## 모수의 해석</br>

* 선형회귀모형에서 회귀계수 : 설명변수의 변화량에 따른 반응변수의 평균변화량</br>

* 비선형회귀모형에서 회귀계수 : 각 모수가 특정한 의미를 가질수 있다.

## 비교
* 선형은 직선 fit
* 비선형은 곡선 fit
