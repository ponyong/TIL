## Spring에서 사용하는 Annotation

```java
@RestController
```
+ 컨트롤러를 JSON으로 반환하는 컨트롤러로 만들어줍니다.

```java
@GetMapping("/hello") {
    return "hello";
}
```

+ Http Method 중 하나인 Get 요청을 받을 수 있는 API를 만들어 줍니다.
+ /hello로 요청이 오면 문자열을 반환하는 기능을 합니다.

```java
@Autowired
```

+ 스프링이 관리하는 빈 (Bean) 을 주입 받습니다.

```java
@Getter
```

+ 선언된 모든 필드의 get 메소드를 생성해 줍니다.

```java
@RequiredArgsConstructor
```

+ 선언된 모든 final 필드가 포함된 생성자를 생성해줍니다.
+ final이 없는 필드는 생성자에 포함되지 않습니다.