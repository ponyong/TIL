## JPA 프로그래밍에 관한 배움을 정리하는 곳입니다.


### JPQL


```SQL

JPQL은 JPA QueryLanguage의 약자로 JPA에서 사용하는 쿼리 언어 이다.
SQL과 매우 유사하지만 테이블과 칼럼이름 대신 매핑한 엔티티 이름과 속성이름을 사용한다는 점이 다르다.

- SQL문 
SELECT 목적 FROM Table명 WHERE 조건문 ORDER BY, GROUP BY 등등 

- JPQL문
SELECT r FROM Review(엔티티 이름) r WHERE r.hotel = :hotel ORDER BY r.id (엔티티 속성 사용) 

- 기본 구조
SELECT 별칭 FROM 엔티티이름 AS 별칭
```

