# String에 대해 기술합니다.

문자열에 해당하는 자료형은 String 으로 표현한다.

즉 문자열을 자바에서 표현하기 위해서는

```java
String a = "Happy Java";

String a = new String("Happy Java");
```

같은 형태로 구현 할 수 있다.

primitive 자료형

int , long , double , float , boolean , char 는 원시 자료형으로

new 키워드를 통해 생성할 수 없다.

원시 자료형은 리터럴로 값을 설정 할 수 있으며

```java
boolean result = true;
char capitalC = 'C';
int i = 100000;
```

와 같이 표현 할 수 있다.

String은 리터럴 하게 표현 할 수 있지만 , 원시 자료형은 아닌 특별한 형태이다.

# String 의 비교

String의 비교는 equals 함수를 활용하여 할 수 있다.

```java
String a = "hello";
String b = "java";
String c = "hello";

a.equals(b); // false
a.equals(c); // true

```

== 연산으로 String을 비교할 경우 값은 같지만 == 는 동일한 객체인지를 판별하는 연산자 이므로 false를 리턴한다.

```java

String a = "hello";
String b = new String("hello");

a.equals(b) // true
a == b // false
```

## StringBuffer || StringBuilder

|               변경               |       동기화        |
| :------------------------------: | :-----------------: |
|             Mutable              |       Mutable       |
| Synchronized 가능 ( Thread-safe) | Synchronized 불가능 |

# StringBuffer , StringBuilder의 특징

- 공통점
  - new 연산으로 클래스가 한번만 만들어짐 ( Mutable )
  * 문자열 연산시 새로운 객체를 만드는 것이 아닌 크기 변경이 이루어짐
  - 클래스의 메소드가 동일하게 이루어져 있음

* 차이점
  - StringBuffer는 Thread-Safe<sup>[1](#Thread-Safe)</sup>함
  - StringBuilder는 Thread-Safe하지 않음

따라서,

StringBuffer는 문자열 연산이 많은 Multi-Thread 환경에서 주로 사용하고,

StringBuilder는 문자열 연산이 많은 Single-Thread 또는 Thread에 신경쓰지 않는 환경에서 주로 사용한다.

<a name="Thread-Safe">Thread-Safe</a>: 멀티스레드 프로그래밍에서 일반적으로 어떤 함수나 변수, 혹은 객체가
여러 스레드로부터 동시에 접근이 이루어져도 프로그램의 실행에 문제가 없음
