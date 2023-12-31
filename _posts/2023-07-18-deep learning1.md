---

layout: post

comments: true

title: 딥러닝 Day1

categories: [딥러닝]

---

# 로지스틱 회귀와 경사하강법



<br>




### 최적화




<br>

최적화는 함수를 minimizing(최소화) 또는 maximizing(최대화)하는 것이다. 

물론 단순하게 minimization(최소화)으로 해석해도 좋다. 

왜냐하면 함수 f(x)의 최솟값(global minimum)을 찾는 것은 -f(x)의 최대값을 찾는 것으로 해석할 수 있기 때문이다.

공학에서의 최적화에 사용되는 함수는 목적함수(objective function)라 한다.

그리고 최적화를 할 때, 만족해야 하는 어떤 조건이 있을 것이다. 

이를 제약조건(constraints)라 한다.

---
### 경사하강법
<br>

최적화 문제를 풀 때, **경사하강법**이라는 알고리즘을 사용할 수 있다.

경사하강법이란 말 그대로 함수의 경사(그래디언트)에 따라 하강하는 것이다.

수식으로 표현하면 뉴턴 랩슨 방법과 유사하다는 것을 알 수 있다.(뉴턴랩슨 방법은 헤시안을 사용하지만 경사하강법은 그래디언트를 사용한다)

$$ w = w - \eta \nabla J(w) $$
1. $w$는 현재의 위치이다.
2. $ \eta$는 학습률이다. 학습률이란 얼마나 갈지를 결정하는 변수이다. 이 변수는 사용자가 임의로 설정할 수 있다.
3. $ \nabla J(w)$ 는 목적함수의 경사(그래디언트)이다. 

<br>

경사하강법을 사용할 때, 목적함수가 convex function(볼록한 함수)라면 무조건 local minimum(지역 최저점) = global minimum(전역 최저점)이 보장된다.

만약 목적함수가 convex function이 아니라면 local minimum = global minimum임이 보장되지 않는다.

그래서 목적함수를 convex function이 아니라면 **convex function으로 함수를 변화**시켜 문제를 풀거나 **경사하강법을 응용한 다른 방법**을 사용하여 global minimum을 찾는다.



---
### 경사하강법의 종류

안타깝게도 많은 최적화 문제의 목적함수는 볼록함수가 아니다. 

따라서 최적화 문제를 풀 때, 어떠한 minimum에 도달했어도 그것이 global minimum이라는 보장을 할 수 없다.

그래서 과학자들과 개발자들은 global minimum에 도달할 수 있는 다양한 경사하강법 알고리즘을 만들었다. 

그중 8가지가 대표적이다.
<br>
1. **Batch gradient descent**: 순정상태의 경사하강법이다. 수식은 다음과 같다
 $$ w = w - \eta \nabla J(w) $$ 
 이 방법을 사용하려면 한번의 업데이트당 한번 함수의 기울기를 계산해야 한다.
 따라서 **상당히 비효율적인 알고리즘**이다. 
 공간 복잡도(프로그램이 메모리를 차지하는 정도)도 상당히 클 수 있고, 시간 복잡도(프로그램이 걸리는 시간)도 클 수 있어 실제 딥러닝과 같은 곳에 사용하기에는 부적합하다.
 또한 local optima에 빠질 경우, 빠져나오는 것이 매우 어렵다
 <br>


2. **Stochastic gradient descent**: 확률적 경사하강법이다. 전체 데이터 셋에서 **한번의 반복에 1개의 샘플**에 대해서만 경사(그래디언트)를 계산한다. 이 방식은 계산 효율성이 높고, noise가 있는 local minima를 건너뛰게 할 수 있다.
이 방법의 단점으로는 계속 원래 가려고 했던 장소를 지나쳐 더 많이 가버릴 수 있어 global minimum으로 수렴하기 힘들어질 수 있다.  이러한 문제는 학습률을 천천히 감소시키면 해결된다고 보인다.<br><br>


3. **Mini-batch gradient descent**: 미니배치 경사하강법이라 한다. 미니 배치 경사하강법은 n개의 미니배치(n을 batch size라 한다)라 하는 작은 집합을 사용하여 병렬로 그래디언트를 계산한다.이 방법은 확률적 경사하강법보다 빠르게 연산된다. 또한 batch 경사하강법보다 덜 건너뛰는 경향이 있다.  batch size는 일반적으로 2**n으로 지정한다. 이 방식의 단점으로는 local minima가 아닌 안장점(saddle point)에서 탈출하기 힘들다는 단점이 있다. 또한 여전히 local minima에서 탈출하기 힘들다는 단점이 있다.<br><br>


4. **momentum**: 모멘텀은 미니배치 경사하강법의 학습률을 변화시키는 것이다.  

5. 

참조: An overview of gradient descent optimization algorithms(https://arxiv.org/pdf/1609.04747.pdf)


---




<br>


### 경사하강법을 코드로 구현

<br>
사실 경사하강법은 


---


### 분류문제란 무엇인가?

<br>


분류 문제란 **연속적이지 않은 변수**를 예측하는 것을 의미한다.

예를 들어서 치와와 사진과 머핀 사진들이 있다고 하자.


![img](https://i.postimg.cc/2SXNWP7f/muffin-meme2.jpg)











이 사진들을 각각 치와와와 머핀으로 구분하는 것이 바로 분류 문제이다. 

치와와와 머핀은 연속적인 변수가 아니다.

이산적인 변수이다.

위와 같은 분류 문제를 Least square과 같은 회귀 알고리즘으로 푸는 것은 좋은 선택이 아니다.

이런 문제를 풀기 위해서는 다른 방법이 필요하다. 

바로 로지스틱 회귀이다.


---
### 로지스틱 회귀와 Sigmoid 함수

<br>
로지스틱 회귀란 회귀(regression)이란 말과 다르게 분류문제를 해결하는 분류 알고리즘 중 하나이다.


방금전에 최적화 문제를 풀 때, 목적 함수가 볼록 함수(convex function)이 아니라면 목적함수를 볼록 함수로 바꾼다는 이야기를 했다. (경사하강법 부분에 나와있다)

여기에서 위와 같은 개념이 사용된다.

이러한 로지스틱 회귀는 딥러닝에서 활성화함수(activation function)으로써 사용된다. 

---


### 로지스틱 회귀를 코드로 구현
```python
import pandas as pd 

for i in range(n):

```
<br>
파이썬을 사용하여 속도가 상당히 느릴 것으로 판단된다.





