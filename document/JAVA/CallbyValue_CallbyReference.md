# Call by Value vs Call by Reference

call by value

```
함수가 호출될 때, 메모리 공간 안에서 함수를 위한 별도의 임시공간이 생성되고 종료시 사라진다.

call by value 호출 방식은 함수 호출 시 전달되는 값을 복사하여 함수 인자로 전달하는데

이때 복사 된 인자는 함수 안에서 지역적으로 사용되기 때문에 local value 속성을 가진다.
```

```java
void call_by_value(int a) {
    a = 20;
}

void main() {
    int n = 10;
    System.out.print(n); // 출력 10
    call_by_value(n);    // 기대값 20
    System.out.print(n); // 출력 10
}
```

함수 내에서 인자 값이 변경되더라도 그 결과가 적용되지 않음
