---

layout: post

comments: true

title: 선형대수학 Day1, 벡터의 정의와 벡터공간

categories: [선형대수학]

---

 
<br>


# 벡터와 벡터 공간
<br>
<br>
## 벡터란 무엇인가?

<br>
<br> 
  많은 사람들한테 벡터를 물어보면 벡터를 크기와 방향을 가진 물리량이라고 이야기한다.
  <br>
  <br>
  하지만 이는 반은 맞고 반은 틀린 이야기이다.
  <br>
  <br>
  벡터의 크기와 방향은 벡터가 가진 기하적인 성질이지, 벡터의 본질적인 표현이 아니다.
<br>
<br>

## 벡터는 벡터공간의 원소이다

<br>

### 벡터공간은 다음과 같은 4가지 연산을 모두 할수있는 원소들의 집합을 벡터공간이라 한다
<br>


1. 덧셈법칙이 정의되어야 한다
2. 스칼라곱이 정의되어야 한다
3. Transpose가 정의되어야 한다
4. 내적이 정의되어야 한다
<br>

이제 4가지 연산에 대해서 차근차근 알아보자.
<br>
<br>

## 덧셈법칙
<br>
덧셈법칙은 우리가 일반적으로 생각하는 a+b=c이다.



다만 조금 더 명확하게는 **항등원과 역원**이 존재하는 연산으로 생각할 수 있다.

항등원은 a+0 = a임은 직관적으로 알 수 있다.

역원은 a+(-a) = 0임또한 직관적으로 알 수 있다.

엄밀하게 설명하자면

1. 결합 법칙을 만족
<br><br>$$ \forall \mathbf{u}, \mathbf{v}, \mathbf{w} \in V, \quad (\mathbf{u} + \mathbf{v}) + \mathbf{w} = \mathbf{u} + (\mathbf{v} + \mathbf{w}) $$<br><br>
벡터 공간 안에 있는 u,v,w에 대하여 위와같은 **결합법칙**이 만족됨
<br><br>


2. 교환 법칙을 만족
<br><br>$$ \forall \mathbf{u}, \mathbf{v} \in V, \quad \mathbf{u} + \mathbf{v} = \mathbf{v} + \mathbf{u} $$<br><br>
벡터 공간 안에 있는 u,v에 대하여 위와같은 **교환법칙**이 만족됨
<br><br>

3. 항등원의 존재
<br><br>$$ \exists \mathbf{0} \in V \text{ such that } \forall \mathbf{v} \in V, \quad \mathbf{v} + \mathbf{0} = \mathbf{v} $$<br><br>
벡터 공간에 있는 v에 대해서 0이라는 **항등원**이 존재한다
<br><br>
4. 역원의 존재
<br><br>$$ \forall \mathbf{v} \in V, \quad \exists \mathbf{-v} \text{ such that } \mathbf{v} + \mathbf{-v} = \mathbf{0}    $$<br><br>
벡터 공간에 있는 v에 대해서 -v이라는 **역원**이 존재한다

<br><br>


즉 벡터공간에서 만족하는 덧셈연산은 항등원과 역원이 존재하고 결합법칙과 분배법칙, 그리고 교환 법칙을 만족한다.



<br>
<br>
## 스칼라곱

스칼라곱은 항등원과 