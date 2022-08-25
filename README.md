# Neural Networks Overview

## 목표
신경망을 어떻게 구현하는지에 대한 개요

## Preview
* logistic regression

<p align="center"> <img src="Neural Networks and Deep Learning/neural network/images/logistic1.PNG"> </p>
<p align="center"> Figure1.logistic regression model </p> </br>

<p align="center"> <img src="Neural Networks and Deep Learning/neural network/images/logistic2-1.PNG"> </p>
<p align="center"> Figure2. compute $z$ </p> </br>
<p align="center"> 1. feature $x$와 parameter $w, b$를 입력하면 $z$를 계산 </p> </br>

<p align="center"> <img src="Neural Networks and Deep Learning/neural network/images/logistic2-2.PNG"> </p>
<p align="center"> Figure3. compute $a$ </p> </br> 
<p align="center"> 2. $z$는 $\hat{y}$이라고 썼던 $a$를 계산 </p> </br>
<p align="center"> <img src="Neural Networks and Deep Learning/neural network/images/logistic1-1.PNG"> </p>
<p align="center"> Figure3. $\hat{y}=a$ </p> </br> 

<p align="center"> <img src="Neural Networks and Deep Learning/neural network/images/logistic2-3.PNG"> </p> </br>
<p align="center"> Figure4. compute $L$ </p> </br> 
<p align="center"> 3. 손실함수 $L$ 을 계산 </p> </br>


## Neural Networks

<p align="center"> <img src="Neural Networks and Deep Learning/neural network/images/nn1.PNG"> </p>
<p align="center"> Figure5. neural network </p> </br> 
> sigmoid unit을 쌓아서 만들 수 있다.


<p align="center"> <img src="Neural Networks and Deep Learning/neural network/images/nn4-1.PNG"> </p>
<p align="center"> Figure6. compute $z^{[1]}$ </p> </br> 
1. feature $x$와 parameter $w, b$를 입력하면 $z^{[1]}$를 계산

* $x^{[i]}$ : i번째 layer
* $x^{(i)}$ : i번째 trainning sample



<p align="center"> <img src="Neural Networks and Deep Learning/neural network/images/nn4-2.PNG"> </p>
<p align="center"> Figure7. compute $a^{[1]}$ </p> </br> 
2. $\sigma (z^{[1]})$ 인 $a^{[1]}$을 계산

<p align="center"> <img src="Neural Networks and Deep Learning/neural network/images/nn4-3.PNG"> </p>
<p align="center"> Figure8. compute $z^{[2]}$ </p> </br> 
3. 다른 선형식을 사용하여 $z^{[2]}$를 계산

<p align="center"> <img src="Neural Networks and Deep Learning/neural network/images/nn4-4.PNG"> </p>
<p align="center"> Figure9. compute $a^{[2]}$ </p> </br> 
4. $\hat{y}$과 같은 neural network의 최종 출력값인 $a^{[2]}$를 계산

## logistic regression와 Neural Network의 차이
### $z, a$ 계산 횟수
- logistic regression : $z, a$를 계산하는 2 step (Figure.1,2)
- Neural Network : $z, a$를 여러번 계산 (Figure.3,4 and Figure.5,6)

### backpropagation

- logistic regression : 


$dz, da$ 계산


- Neural Network : 

1. $da^{[2]}$ 계산

2. $ dz^{[2]} $ 계산
3. $da^{[2]}$ , dz^{[2]} $를 가지고 $ dW^{[2]}, db^{[2]} $ 계산
4. 
 
