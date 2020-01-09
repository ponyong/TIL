# 이진 탐색 알고리즘

## <이 알고리즘으로 해결하고자 하는 것>

```
오름차순으로 정렬된 리스트에서 특정 값의 위치를 찾는 알고리즘
```

## <핵심 이론>
```
중간값을 기준으로 탐색의 범위를 반씩 줄여 탐색의 시간을 줄인다.
```
## <핵심 변수>

```java
int low, high, mid // 인덱스 변수
int target         // 타겟 넘버
```
## <핵심 코드>
```java
//반복문으로 구현한 binarySearch
int BinarySearch(int arr[], int target) {
    int low = 0;
    int high = arr.length - 1;
    int mid;

    while(low <= high) {
        mid = (low + high) / 2;

        if (arr[mid] == target)
            return mid;
        else if (arr[mid] > target)
            high = mid - 1;
        else
            low = mid + 1;
    }
    return -1;
}
```

```java
// 재귀로 구현한 binarySearch
int BinarySearchRecursive(int arr[], int target, int low, int high) {
    if (low > high)
        return -1;

    int mid = (low + high) / 2;
    if (arr[mid] == target)
        return mid;
    else if (arr[mid] > target)
        return BinarySearchRecursive(arr, target, low, mid-1);
    else
        return BinarySearchRecursive(arr, target, mid+1, high);
}
```
## <알고리즘 진행 순서>

```
1. 배열의 중간값 ( low + high / 2 ) 과 찾고자 하는 값 ( target ) 을 비교한다.

2. 중간 값이 target 보다 크다면 작은 쪽의 탐색을 버리는 것으로 탐색의 시간을 줄인다.

3. 결과 값을 찾을 때까지 위의 1 ~ 2 과정을 반복
```
## <시간 복잡도 및 최적화 개선사항>

```
한번의 연산에서 절반 씩 범위가 줄어들기 때문에 O(logN) 의 시간에 탐색을 완료 할 수 있다.
```