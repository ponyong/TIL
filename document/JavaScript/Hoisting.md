# 호이스팅(Hoisting)에 대해 기술합니다.

# 정의

- 함수 안에 있는 모든 선언들을 끌어올려 해당 함수 유효 범위의 최상단에 선언하도록 하는것

* 선언과 할당의 구분을 편의적으로 지원하는 기술

- 자바스크립트 함수는 실행 전 함수 내에 필요한 변수값들을 모두 모아 유효 범위 최상단에 선언한다.
  - 프로그램 실행시 Parser가 함수 실행 전 해당 함수를 읽는다.
  - 함수 안에 존재하는 변수 , 함수선언에 대한 정보를 기억하고 있다가 실행한다.

* 함수 내에서 아래 쪽에 존재하는 내용을 끌어올리는 것이다.
  - 실제로 끌어올려지는 것은 아니고 , Parser가 내부적으로 끌어올려 처리하는 것
  - 실제 메모리에서는 변화가 없음

# 적용 대상

- var 변수 선언 , "함수 선언문"에서만 호이스팅이 발생한다.
  - "선언" 만 위로 끌어올려지고 , "할당"은 끌어올려지지 않는다.

* let / const 변수와 "함수 표현식" 에서는 호이스팅이 발생하지 않는다.

== 사용자가 작성한 코드 ( var vs let / const ) ==

```javascript
console.log("Test");
var test1 = "hello";
let test2 = "hello2";
```

== 호이스팅이 일어난 코드 ==

```javascript
var test1;
console.log("Test");
test1 = "hello";
let test2 = "hello2";
```

== 사용자가 작성한 코드 ( 함수 표현식 vs 함수 선언문 ) ==

```javascript
foo();
foo2();

function foo() {
  console.log("hello");
}

var foo2 = function () {
  console.log("hello2");
};
```

== 호이스팅이 일어난 코드 ==

```javascript
var foo2;

function foo() {
  console.log("hello");
}

foo();
// 변수에 할당되는 함수 표현식은 호이스팅이 일어나지 않기 때문에
// 아직 읽히지 않은 foo2는 선언되지 않았으므로 Error가 발생한다.
foo2();

foo2 = function () {
  console.log("hello2");
};
```
