## Queue

```

컴퓨터의 기본적인 자료 구조 중 한가지

먼저 집어 넣은 데이터가 먼저 나오는 FIFO ( First In First Out ) 선입 선출 구조를 가진다.

```

Queue 의 주요 연산


```java
Queue<value> queue = new LinkedList<>();

queue.add(value): value 값을 리스트의 끝 부분에 추가한다.

queue.remove(): 리스트의 첫 번째 항목을 제거한다.

queue.peek(): 큐에서 가장 위에 있는 항목을 반환한다. ( 리스트에 변경 없음 )

queue.isEmpty(): 큐가 비어 있을 때에 true를 반환한다.

```
