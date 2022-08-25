# Neural Network Overview

## 학습목표
Neural Network을 어떻게 구현하는지에 대한 개요

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
<p align="center"> 1. feature $x$와 parameter $w, b$를 입력하면 $z^{[1]}$를 계산 </p> 

<p align="center"> <img src="Neural Networks and Deep Learning/neural network/images/nn3.PNG"> </p>
<p align="center"> Figure7. layer $[1],[2]$ </p> </br> 

* $x^{[i]}$ : i번째 layer
* $x^{(i)}$ : i번째 trainning sample


<p align="center"> <img src="Neural Networks and Deep Learning/neural network/images/nn4-2.PNG"> </p>
<p align="center"> Figure8. compute $a^{[1]}$ </p>
<p align="center"> 2. $\sigma (z^{[1]})$ 인 $a^{[1]}$을 계산 </p> 


<p align="center"> <img src="Neural Networks and Deep Learning/neural network/images/nn4-3.PNG"> </p>
<p align="center"> Figure9. compute $z^{[2]}$ </p>
<p align="center"> 3. 다른 선형식을 사용하여 $z^{[2]}$를 계산 </p> 


<p align="center"> <img src="Neural Networks and Deep Learning/neural network/images/nn4-4.PNG"> </p>
<p align="center"> Figure10. compute $a^{[2]}$ </p>
<p align="center"> 4. $\hat{y}$과 같은 neural network의 최종 출력값인 $a^{[2]}$를 계산 </p> 

<p align="center"> <img src="Neural Networks and Deep Learning/neural network/images/neuralnetworks2.PNG"> </p>
<p align="center"> Figure11. $\hat{y}=a^{[2]}$ </p> </br> 


## logistic regression와 Neural Network의 차이
### 1. $z, a$ 계산 횟수
- logistic regression : $z, a$를 계산하는 2 step (Figure2,3)
- Neural Network : $z, a$를 여러번 계산 (Figure7,8 and Figure9,10)

### 2. backpropagation
- logistic regression : $dz,da$ 계산

<p align="center"> <img src="Neural Networks and Deep Learning/neural network/images/logistic-back.PNG"> </p>
<p align="center"> Figure10. compute $dz, da$ </p> </br>


- Neural Network : $da^{[2]}$ , dz^{[2]}, dW^{[2]}, db^{[2]} $
<p align="center"> <img src="Neural Networks and Deep Learning/neural network/images/nn-back1.PNG"> </p>
<p align="center"> Figure11. compute $da^{[2]}$ </p>
<p align="center"> 1. $da^{[2]}$ 계산 </p> </br>

<p align="center"> <img src="Neural Networks and Deep Learning/neural network/images/nn-back2.PNG"> </p>
<p align="center"> Figure12. compute $ dz^{[2]} $ </p>
<p align="center"> 2. $ dz^{[2]} $ 계산 </p>

<p align="center"> <img src="Neural Networks and Deep Learning/neural network/images/nn-back3.PNG"> </p>
<p align="center"> Figure13. compute $ dW^{[2]}, db^{[2]} $ </p>
<p align="center"> 3. $da^{[2]}$ , dz^{[2]} $를 가지고 $ dW^{[2]}, db^{[2]} $ 계산 </p> 

---
# 참고
[Andrew Ng-Neural Network Overview]([https://www.youtube.com/watch?v=CcRkHl75Z-Y&list=PLkDaE6sCZn6Ec-XTbcX1uRg2_u4xOEky0&index=26](https://www.youtube.com/watch?v=fXOsFF95ifk&list=PLkDaE6sCZn6Ec-XTbcX1uRg2_u4xOEky0&index=25))
