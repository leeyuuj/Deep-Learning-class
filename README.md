# Neural Networks Overview

## 목표
신경망을 어떻게 구현하는지에 대한 개요

## Preview
* logistic regression

<p align="center"> <img src="images/logisticreg1.PNG"> </p> </br>
Figure1.logistic regression model

1. feature $x$와 parameter $w, b$를 입력하면 $z$를 계산

<p align="center"> <img src="images/logisticreg2.PNG"> </p> </br>

2. $z$는 $\hat{y}$이라고 썼던 $a$를 계산하는데 쓰인다.
3. 손실함수 $L$을 계산

### logistic regression 특징
- $z, a$를 계산하는 2 step

## 신경망
sigmoid unit을 쌓아서 만들 수 있다.

1. feature $x$와 parameter $w, b$를 입력하면 $z^{[1]}$를 계산
> $ x^{[i]} $ : i번째 layer

> $ x^{(i)} $ : i번째 trainning sample

2. 
