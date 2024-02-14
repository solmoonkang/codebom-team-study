# *Exhaustive Search Algorithm*, 완전 탐색 알고리즘

## *Exhaustive Search*, 완전 탐색이란?

---

*Exhaustive Search* 은 **‘모든 가능한 경우의 수를 탐색’**하여 **‘최적의 결과를 찾는 방법’**을 의미한다.

- 모든 가능성을 고려하기 때문에 항상 최적의 해를 찾을 수 있다.
- 하지만 경우의 수가 많은 경우 시간과 메모리의 부담이 커질 수 있다.

즉, *Exhaustive Search* 는 무식하게 가능한 것들을 다 시도해보겠다는 방법을 의미한다.

<aside>
📌 무식하게 모든 방법들을 다 한다는 의미로 *“Brute Force”* 라고도 부른다.

</aside>

## *Exhaustive Search* 종류

---

*Exhaustive Search* 기법으로 문제를 풀기 위해서는 다음과 같은 경우를 고려해서 수행해야 한다.

1. 해결하고자 하는 문제의 가능한 경우의 수를 대략적으로 계산한다.
2. 가능한 모든 방법을 다 고려한다.
3. 실제 답을 구할 수 있는지 적용한다.

### *Brute Force*, 브루트 포스

---

브루트 포스 기법은 반복 / 조건문을 통해 가능한 모든 방법을 단순히 찾는 경우를 의미한다.

예를 들어, 4자리의 암호로 구성된 자물쇠를 풀려고 시도한다고 가정해보자. 이 자물쇠가 고장난 것이 아니라면, 반드시 해결할 수 있는 가장 확실한 방법은 0000 ~ 9999 까지 모두 시도해보는 것이다.

### *Bitmask*, 비트마스크

### *Backtracking*, 백트래킹

### *Permutation*, 순열

---

순열이란 ‘임의의 수열이 있을 때, 그것을 다른 순서로 연산하는 방법’을 의미한다.

- 즉, 순서가 중요하다. 수열에서 [1, 2, 3]과 [3, 2, 1]로 보는 순서에는 차이가 있다.
- 같은 데이터가 입력된 수열이지만, 순서에 따라 의미가 있고 이 순서를 통해 연결되는 이전 / 다음 수열을 찾아낼 수 있는 경우를 계산할 수 있다.

### *Recursive Function*, 재귀함수

---

재귀란 말 그대로 ‘자기 자신을 호출’한다는 의미이다.

### *Depth-First Search, DFS / Breadth-First Search, BFS*