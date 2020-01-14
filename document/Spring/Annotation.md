# Spring에서 사용하는 Annotation

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
@NoArgsConstructor
```


Required
+ 선언된 모든 final 필드가 포함된 생성자를 생성해줍니다.
+ final이 없는 필드는 생성자에 포함되지 않습니다.

No
+ 기본생성자 자동 추가
+ public class() {} 와 같은 효과

```java
@RequestParam
```

+ 외부에서 api 로 넘긴 파라미터를 가져오는 Annotation 입니다.


# JPA에서 제공하는 Annotation

```java
@Entity
```

+ 테이블과 링크될 클래스 입니다.
+ 클래스의 카멜케이스 이름을 언더스코어 네이밍으로 테이블 이름을 매칭합니다
    + ex) SalesManager.java -> sales_manager table 로 변환

```java
@Id
```

+ 해당 테이블의 PK를 나타냅니다.

```java
@GeneratedValue
```

+ PK의 생성 규칙을 나타냅니다.
+ 스프링 부트 2.0에서는 GenerationType.IDENTITY 옵션을 추가해야 auto_increment가 됩니다.


```java
@Column
```

+ 테이블의 칼럼을 나타내며 굳이 선언하지 않아도 해당 클래스의 필드는 모두 칼럼이 됩니다.
+ 기본값 외에 추가로 변경이 필요한 옵션이 있는 경우에 사용합니다.