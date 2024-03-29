# Brute Force

- **완전 탐색 알고리즘**
- 즉, 가능한 모든 경우의 수를 모두 탐색하면서 요구조건에 충족되는 결과만을 가져온다.
- 강력한 점 : 예외 없이 100%의 확률로 정답만을 출력.

### 일반적 방법
- 문제를 해결하기 위해서는 모든 자료를 탐색해야 하기 때문에 특정한 구조를 전체적으로 탐색할 수 있는 방법을 필요.
- 기본적인 접근 방법 : 해가 존재할 것으로 예상되는 모든 영역을 전체 탐색하는 방법. 
- 가장 기본적인 도구 종류
  - 선형 구조를 전체적으로 탐색하는 순차 탐색
  - 비선형 구조를 전체적으로 탐색하는 깊이 우선 탐색(DFS, Depth First Search) -> 백트레킹과 관련 높음
  - 비선형 구조를 전체적으로 탐색하는 너비 우선 탐색(BFS, breadth first search) -> 브루트포스와 관련 높음

### 문제해결 방법
1. 주어진 문제를 선형 구조로 구조화 
2. 구조화된 문제공간을 적절한 방법으로 해를 구성할 때까지 탐색 
3. 구성된 해를 정리

### 예제 - 10의 약수합
1. 10의 약수 구조화
    - {1, 2, 3, 4, 5, 6, 7, 8, 9, 10}
    - 문제의 해가 될 수 있는 자료를 선형 구조로 구성
2. 구조화 자료가 선형 구조이다. 즉, 순차 탐색을 활용하여 첫 번째 원소부터 마지막 원소까지 탐색 
   - 10의 약수가 되는 값만 남겨두고 10의 약수가 될 수 없는 값을 배제.
3. 위의 과정 반복.
```java
    int sum = 0;

    for(int i=1; i <= 10; i++){
        if(n % i == 0)
            sum += i;
    }
```

