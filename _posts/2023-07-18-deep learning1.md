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

## 벡터는 벡터공간(Vector Space)의 원소이다

<br>

---

### 벡터공간은 다음과 같은 4가지 연산을 모두 할수있는 원소들의 집합을 벡터공간이라 한다
<br>


1. 덧셈법칙이 정의되어야 한다
2. 스칼라배가 정의되어야 한다
3. Transpose가 정의되어야 한다
4. 내적이 정의되어야 한다
<br>

이제 4가지 연산에 대해서 차근차근 알아보자.
<br>
<br>

---

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
벡터 공간 안에 있는 u,v에 대하여 위와같은 **교환법칙**이 만족된다
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

---

<br>
<br>
## 스칼라배(scalar multiple)

스칼라배는 벡터와 스칼라에 대한 연산이다.

벡터의 방향을 보존하면서 벡터의 길이를 스칼라의 절대값만큼 늘리거나, 줄인다고 생각할 수 있다. 


이것또한 교환 법칙, 결합 법칙을 만족한다.

1. 교환 법칙
$$  c \cdot (a \cdot \mathbf{v}) = (c \cdot a) \cdot \mathbf{v} $$
<br>
<br>
c와 a는 스칼라이고 v는 벡터이고 다음과 같이 교환법칙이 성립한다는 것을 알 수 있다
<br>
<br>

2. 결합 법칙
$$  (c_1 \cdot c_2) \cdot \mathbf{v} = c_1 \cdot (c_2 \cdot \mathbf{v}) $$<br><br>
스칼라배도 결합법칙이 만족되는 연산임을 알 수 있다.

<br>
<br>


스칼라배에서 조심해야 할 것은 **스칼라배(scalar multiple)은 스칼라곱(scalar product)이 아니다** 라는 점이다.


<br>

---
## 전치(Transpose)

전치는 벡터를 돌린 것이라고 생각할 수 있다.


$$
\begin{pmatrix}
a_1 \\
a_2 \\
a_3
\end{pmatrix}^\intercal
= [a_1 \quad a_2 \quad a_3]
$$

---
## 내적(Dot product)


내적을 정의하자면

$$ 
\mathbf{a} = \begin{bmatrix} a_1 \\ a_2 \\ \vdots \\ a_n \end{bmatrix}, \quad
\mathbf{b} = \begin{bmatrix} b_1 \\ b_2 \\ \vdots \\ b_n \end{bmatrix}
$$

라는 벡터 a,b가 있다고 하자.

이 a,b의 내적은 다음과 같이 정의된다. 

$$
\mathbf{a} \cdot \mathbf{b} = a_1 b_1 + a_2 b_2 + \ldots + a_n b_n
$$

<br>

>여기에서 우리는 내적에 대한 중요한 사실 2가지를 알 수 있다. <br><br>첫번째로 내적은 **차원이 같은 두 벡터간의 연산**이다.<br>
차원이 다르다면 내적을 할 수 없는 것이다.<br>
두번째로 **내적은 벡터와 벡터의 연산으로 스칼라를 출력**하는 연산이다

<br>
<br>

벡터의 내적도 **교환법칙과 결합법칙**이 성립한다.

1. 교환법칙
$$
\mathbf{a} \cdot \mathbf{b} = \sum_{i=1}^{n} a_i b_i = \sum_{i=1}^{n} b_i a_i = \mathbf{b} \cdot \mathbf{a}
$$
<br>
차원이 같은 두 벡터 a,b에 대해서 교환법칙이 만족함을 알 수 있다.
<br>
<br>
2. 결합법칙
$$
(\mathbf{a} \cdot \mathbf{b}) \cdot \mathbf{c} = \left(\sum_{i=1}^{n} a_i b_i\right) \cdot \mathbf{c} = \sum_{i=1}^{n} (a_i b_i) c_i = \mathbf{a} \cdot (\mathbf{b} \cdot \mathbf{c})
$$
<br>
차원이 같은 두 벡터 a,b에 대해서 결합법칙이 만족함을 알 수 있다.
<br>
<br>

또한 벡터의 내적의 다른 표현은 다음과 같이 정의된다.<br><br>
$$
\mathbf{a} \cdot \mathbf{b} = \mathbf{a}^T \mathbf{b} = \begin{bmatrix} a_1 & a_2 & \ldots & a_n \end{bmatrix} \begin{bmatrix} b_1 \\ b_2 \\ \vdots \\ b_n \end{bmatrix}
$$
<br><br>
즉 우리는 Transpose(전치)를 정의함으로써 벡터의 내적에 다른 표현이 있다는 것을 알 수 있다. 

벡터의 내적을 편하게 하려면 ㄱ을 생각하면 된다. 벡터의 내적은 항상 **ㄱ자 연산**이다.


---
<br>

## Norm(노름)

노름은 벡터의 크기를 측정하는 방법이다. <br><br>노름에는 여러가지 종류가 있지만 우리가 알아야 할 노름은 Euclidean Norm(L2 Norm)이다

L2 Norm은 한마디로 점과 점사이의 거리공식을 확장시킨 것이라 생각하면 된다. 

n차원의 벡터 a에 대해서 L2 Norm은 다음과 같이 정의된다.

$$ \| \mathbf{a} \|_2 = \sqrt{\sum_{i=1}^{n} a_i^2} $$

이는 내적으로 다시 정의하면
$$
\| \mathbf{a} \|_2 = \sqrt{\mathbf{a} \cdot \mathbf{a}}
$$
<br>
<br>
또한 내적을 Transpose로 정의할 수 있으므로 다음과 같이 표현할 수 있다.
<br>
<br>
$$
\mathbf{a} \cdot \mathbf{b} = \mathbf{a}^T \mathbf{b}
$$
<br>
<br>

---



## 내적을 Norm으로써 다시 정의

내적은 다음과 같이 Norm과 각 θ로 표현될 수 있다.

<br>
<br>

$$
\mathbf{a} \cdot \mathbf{b} = \|\mathbf{a}\| \|\mathbf{b}\| \cos(\theta)
$$
<br>
<br>

여기에서 알아야 할 것은 각 θ는 두 벡터 a,b가 이루는 각이다. 

즉 두 벡터 a,b가 수직한 관계에 있으면 cosθ=0이 되므로 내적이 항상 0이 됨을 알 수 있다.


---



## 연습 문제


### 1번

벡터 a,b 에 대해서 a+b를 구하시오.



### 2번

다음조건을 만족하는 벡터 a,b 에 대해서 a를 b로 표현하시오.

### 3번

2가 scalar이고 a는 벡터라 한다면 2a는 a의 스칼라배라고 할 수 있다. 

여기에서 a+a = 2a이므로 벡터의 덧셈법칙으로 스칼라배를 표현 할 수 있다는 것을 알 수 있다

그러면 임의의 실수 C에 대해서 왜 스칼라배 Ca는 Ca = a+a+a+... 와 같이 덧셈법칙으로 표현 할 수 없는지 증명하시오.

### 4번

서로 수직임을 보이시오


### 5번

word count 벡터는 다음과 같이 정의된다.
예를 들어 I want to go to the moon 이라는 문장이있다고 하자. 
그러면 I:1번 want: 1번, to: 2번, the:1번, moon: 1번으로 
이 문장의 word count 벡터는 [1,2,2,1,1] 로 정의된다. 이때 


### 6번

세 점 A(a1,a2,a3), B(b1,b2,b3), C(c1,c2,c3)에 대해서 세 점과의 거리가 최소화되는 점 P(p1,p2,p3)를 a1,a2,a3,b1,b2,b3,c1,c2,c3로 표현하시오.

>Hint 거리는 유클리디언 Norm이다. 


<details>
<summary>연습 문제의 정답, 눌러서 확인</summary>

## 연습 문제 정답


### 1번

벡터 a,b 에 대해서 a+b를 구하시오.



### 2번

다음 조건을 만족하는 벡터 a,b 에 대해서 a를 b로 표현하시오.

### 3번

2가 scalar이고 a는 벡터라 한다면 2a는 a의 스칼라배라고 할 수 있다. 

여기에서 a+a = 2a이므로 벡터의 덧셈법칙으로 스칼라배를 표현 할 수 있다는 것을 알 수 있다

그러면 임의의 실수 C에 대해서 왜 스칼라배 Ca는 Ca = a+a+a+... 로 표현 할 수 없는지 증명하시오.

### 4번

서로 수직임을 보이시오
</details>