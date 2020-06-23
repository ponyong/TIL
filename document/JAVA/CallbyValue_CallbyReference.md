# Call by Value vs Call by Reference

# Call by value

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

# Call by Reference

```
함수가 호출될 때, 인자로 전달되는 변수의 레퍼런스를 전달한다.

따라서 함수 안에서 값이 변경되면 전달한 원본 객체의 값도 변경 된다.
```

```java
void call_by_reference(int *a) {
    *a = 20;
}

void main() {
    int n = 10;
    System.out.print(n); // 출력 10
    call_by_reference(&n); // 기대값 20
    System.out.print(n);  // 출력 20
}
```

# JAVA에서 함수 호출하는 방식

전달되는 인자의 데이터 타입에 따라 함수 호출 방식이 바뀐다.

- 원시 자료형( Primitive type ) : call by value
  | int , short, long , float, double , char , boolean

* 참조 자료형( Reference type) : call by reference
  | array , Class instance, String

Call by value의 경우, 데이터 값을 복사해서 함수로 전달하기 때문에 원본의 데이터가 변경될 가능성이 없다.
하지만 인자를 넘겨줄 때마다 메모리 공간을 할당해야해서 메모리 공간을 더 잡아먹는다.

Call by reference의 경우 메모리 공간 할당 문제는 해결했지만, 원본 값이 변경될 수 있다는 위험이 존재한다.
