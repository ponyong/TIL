# Heap

```

우선 순위 큐 ( Priority Queue ) 를 위해 만들어진 자료구조

배열을 이용하여 힙을 구현 할 수 있다.

```

| 구현 방법            |  삽입   |    삭제 |
| -------------------- | :-----: | ------: |
| 순서 없는 배열       |  O(1)   |    O(n) |
| 순서 없는 연결리스트 |  O(1)   |    O(n) |
| 정렬된 배열          |  O(n)   |    O(1) |
| 정렬된 연결리스트    |  O(n)   |    O(1) |
| 힙                   | O(logn) | O(logn) |

```
완전 이진 트리의 일종

여러 개의 값 중 최소, 최대 값을 빠르게 찾아 낼 수 있는 자료구조

완전한 정렬이 아닌 반정렬 상태를 유지한다.

=> 큰 값이 위 , 작은 값이 아래에 있다는 정도 완벽한 정렬을 필요로 하지는 않는다.
```