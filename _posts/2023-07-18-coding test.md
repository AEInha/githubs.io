---

layout: post

comments: true

title: 알고리즘 풀이 백준 2225 합분해

categories: [알고리즘]

---

# 문제

---
0부터 N까지의 정수 K개를 더해서 그 합이 N이 되는 경우의 수를 구하는 프로그램을 작성하시오.

덧셈의 순서가 바뀐 경우는 다른 경우로 센다(1+2와 2+1은 서로 다른 경우). 또한 한 개의 수를 여러 번 쓸 수도 있다.


<br>

## 입력
<br>

첫째 줄에 두 정수 N(1 ≤ N ≤ 200), K(1 ≤ K ≤ 200)가 주어진다.


<br>
<br>

## 출력



<br>
첫째 줄에 답을 1000000000으로 나눈 나머지를 출력한다.

<br>
<br>
<br>
<br>
<br>
<details>
<summary>연습 문제의 정답, 눌러서 확인</summary>

~~~python
n,k = map(int,input().split())
dp = [1 for i in range(n)]

if k ==1:
  print(1)
else:
  for j in range(1,k):
    for i in range(n):
      if i == 0:
        dp[i] = (j+1)%1000000000
      else:
        dp[i] = (dp[i-1]+dp[i])%1000000000
  print(dp[n-1]%1000000000)

~~~


---


위 코드는 동적 프로그래밍을 사용했다.

dp[i] = dp[i-1](k번째의 i)+dp[i](k-1번째의 i), 이때 (1<i<n) 라는 점화식을 세워 문제를 풀었다.
</details>

<br>
동적 프로그래밍을 할 때, 어떻게 설계해야 하는지 알수 있었던 문제였다.

점화식을 만들 때, 애를 좀 먹었다.