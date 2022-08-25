# Neural Network Representation
<p align="center"> <img src="Neural Networks and Deep Learning/neural network/images/2nn1.PNG"> </p>
<p align="center"> Figure1.Neural Network </p> </br>

## input layer (입력층) 
<p align="center"> <img src="Neural Networks and Deep Learning/neural network/images/inputlayer.PNG"> </p>
<p align="center"> Figure2.input layer </p> </br>

* feature $x_1, x_2, x_3$ 이 세로로(vertically) 쌓여있는 층

## hidden layer (은닉층)
<p align="center"> <img src="Neural Networks and Deep Learning/neural network/images/hiddenlayer.PNG"> </p>
<p align="center"> Figure3.hidden layer </p> </br>


 - 지도학습으로 훈련시키는 신경망에선 훈련세트가 X,Y로 이루어져있고 은닉층의 실제값은 훈련세트에 기록되어있지 않다.
 - 입력값, 출력값은 알수있지만 은닉층의 값은 알 수 없다.
 - 은닉층이라는 이름은 훈련세트에서 볼 수 없다는 것을 의미한다.
 
## output layer (출력층) 
<p align="center"> <img src="Neural Networks and Deep Learning/neural network/images/outputlayer.PNG"> </p>
<p align="center"> Figure4.output layer </p> </br>

* $\hat{y}$의 계산을 책임진다.

## $a$로 보는 layer
1. input layer

<p align="center"> <img src="Neural Networks and Deep Learning/neural network/images/inputl1.PNG"> </p>
<p align="center"> Figure5.input layer1 </p> </br>

>  $a$ : 활성값, 신경망의 층들이 다음 층으로 전달해주는 값 </br>
>  $a^{[0]}=X$ </br>
>  $a^{[0]}$ : 입력층의 활성값

2. hidden layer

<p align="center"> <img src="Neural Networks and Deep Learning/neural network/images/hiddenl1.PNG"> </p>
<p align="center"> Figure6.hidden layer1 </p> </br>

>  $a^{[1]}$ = 
$\begin{bmatrix}
a_1^[1]\
a_2^[1]\
a_3^[1]\
a_4^[1]\
\end{bmatrix}$ 인 (1, 4)인 matrix or column vector
은닉노드가 4개이기때문에 4차원이다.

3. output layer
<p align="center"> <img src="Neural Networks and Deep Learning/neural network/images/outputl1.PNG"> </p>
<p align="center"> Figure7.output layer1 </p> </br>

>  $a^{[2]}=\hat{y}$ </br>
>  logistic regression에서 $\hat{y}=a$인 것과 비슷하다.

* 신경망의 층을 셀때 입력층은 세지 않기때문에 이 신경망은 2 layer NN (2층 신경망)이다.
은닉층이 1번째, 출력층이 2번째 (표기관례상 입력층: 0번째 층)
이 신경망엔 입력층, 은닉층, 출력층 층이 3개 있다고 할수있지만 관례적으로 이 신경망을 2 layer NN (2층 신경망)이라 부를것이다.

* 은닉층과 출력층은 연관된 parameter가 있다. 
- 은닉층: $w^{[1]}, b^{[1]}$  (1번째 은닉층에 관련된 parameter : 윗첨자 [1]을 붙임) </br>
$ w^{[1]} = (4,3) $ </br>
> 은닉노드 4개, feature 3개 </br>
$ b^{[1]} = (4,1) $ 

- 출력층: $w^{[2]}, b^{[2]}$ </br>
$ w^{[2]} = (1,4) $ </br>
> 출력노드 1개, 은닉노드 4개
$ b^{[2]} = (1,1) $ 


---
# 참고
[Andrew Ng](https://www.youtube.com/watch?v=CcRkHl75Z-Y&list=PLkDaE6sCZn6Ec-XTbcX1uRg2_u4xOEky0&index=26)
