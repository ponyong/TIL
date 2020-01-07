# 다익스트라 알고리즘

## <이 알고리즘으로 해결하고자 하는 것>

```
그래프 구조에서 최단거리를 구하는 알고리즘
```

## <핵심 이론>

``` 
하나의 시작 정점에서 다른 모든 정점으로의 최단거리를 계산 한다.
```

## <핵심 변수>

```java
distance[] // 최단 거리를 저장 할 수 있는 변수
check[] // 해당 정점을 방문했는지 체크 할 수 있는 Bool 변수
```

## <핵심 코드>
```java

        //distance 배열의 초기화
        for(int i = 1; i < N+1; i++){
            distance[i] = Integer.MAX_VALUE;
        }
        //시작노드값 초기화.
        distance[v] =0;
        check[v] = true;
         
        //연결노드 distance 값을 갱신
        for(int i = 1; i < N+1;i++){
            if(!check[i] && maps[v][i] !=0){
                distance[i] = maps[v][i];
            }
        }
         
         
        //노드가 N개 있을 때 N-1번 반복하면 된다.
        for(int a = 0; a < N-1;a++){
            int min = Integer.MAX_VALUE;
            int min_index = -1;
             
            //최소값 찾기
            for(int i = 1; i <N+1; i++){
                if(!check[i] && distance[i] != Integer.MAX_VALUE){
                    if(distance[i] < min ){
                        min = distance[i];
                        min_index = i;
                    }
                }
            }
            // 값 갱신 
            check[min_index] = true;
            for(int i=1; i < n+1; i++){
                if(!check[i] && maps[min_index][i] != 0){
                    if(distance[i] > distance[min_index] + maps[min_index][i]){
                        distance[i] = distance[min_index] + maps[min_index][i];
                    }
                }
            }
        }
```
## <알고리즘 진행 순서>
```
    1. 거리 배열( distance ) 를 가장 큰 값으로 초기화
    2. 시작 정점 거리를 0으로 변경
       시작 정점의 check 값을 true 로 변경
    3. 시작 정점과 연결 된 정점들의 distance 값을 갱신
    4. 방문하지 않은 노드 중 distance 값이 최소인 정점 탐색 ( Greedy )
    5. 찾은 정점의 check값 ture로 변경, 연결된 노드의 distance를
       해당 정점의 현재 값과 계산한 값을 비교하여 작은 값으로 갱신

    모든 노드를 방문 할 때까지 반복 실행 
```

## <시간 복잡도 및 최적화 개선사항>
```
정점의 개수가 일정 이상 커지게 되면 O(n^2) 의 시간이 소요되어
시간 초과 문제가 발생 할 수 있음

최소 값을 찾는 과정에서 PQ(우선순위 큐)를 사용하여 검색 시간을 O(logN)으로 해결
```