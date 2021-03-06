### MarkDown 기본문법

# 0. TEXT 박스 ( 주석 개념 )

```
    `(그레이브) 세개로 TEXT 를 감싸주게 되면 텍스트 박스 형태로 저장됩니다.
```

# 1. HEADER (머리말)

```
# 의 개수로 글씨의 크기를 조절 할 수 있습니다.
1~6개 까지 지원하며 여러개를 사용 할 수록 크기가 작아집니다.
```

# TEST is H1

## TEST is H2

### TEST is H3

# 2. 강조 ( Emphasis )

```
각각 <em> <strong> <del> 태그로 변환됩니다.

밑줄은 <u></u> 태그를 사용합니다.
```

```
이텔릭체는 * 혹은 _ 를 사용합니다.
ex) * Example *

볼드체는 ** 혹은 __ 를 사용합니다.
ex) ** Example **

두가지를 혼합하여 사용 할 수 있습니다.
ex) **_ Example _**

취소선은 물결표시를 사용합니다.
ex) ~~ Example ~~

밑불은 <u></u> 를 사용합니다.
ex) <u> Example </u>
```

_이텔릭체_ <br>
**볼드체** <br>
**_혼합_** <br>
~~취소선~~ <br>
<u>밑줄</u> <br>

# 3. 목록 (List)

```
<ol> <ul> 목록 태그로 번환됩니다.
```

순서가 필요한 리스트는 숫자와 점으로 표기합니다.
같은 숫자를 사용하여도 오름차순으로 정렬됩니다.
순서가 필요하지 않은 리스트는 기호로 표기합니다.

```
대쉬 ( - )
별표 ( * )
더하기 ( + )
```

    1.  순서가 필요한 목록
    2.  순서가 필요한 목록
        - 순서가 필요없는 목록
        - 순서가 필요없는 목록

# 4. 링크 ( Links )

```
<a> 태그로 변환 됩니다.
```

```
[GOOGLE](https://google.com) 일반적인 링크

[NAVER](https://naver.com "링크 설명 ( 마우스 올렸을때 나오는 텍스트) 를 작성하세요.")

문서 안에서 [참조 링크] 를 그대로 사용 할 수 있습니다.

문서 안에서 일반 URL , <  > 안의 URL은 자동으로 링크를 사용합니다.

[참조 링크]: https://naver.com "네이버로 이동"
```

[GOOGLE](https://google.com) <br>
[NAVER](https://naver.com "네이버로 연결됩니다.") <br>

문서 내에서 [참조 링크] 사용 <br>

[참조 링크]: https://naver.com "네이버 이동"

# 5. 표 ( table )

```
<table> 태그로 변환 됩니다.

헤더 셀을 구분할 때 3개 이상의 -(hyphen/dash) 기호가 필요합니다.
헤더 셀을 구분하면서 :(Colons) 기호로 셀(열/칸) 안에 내용을 정렬할 수 있습니다.
가장 좌측과 가장 우측에 있는 |(vertical bar) 기호는 생략 가능합니다.
```

| 값         |                  의미                  |   기본값 |
| ---------- | :------------------------------------: | -------: |
| `static`   |     유형(기준) 없음 / 배치 불가능      | `static` |
| `relative` |       요소 자신을 기준으로 배치        |          |
| `absolute` | 위치 상 부모(조상)요소를 기준으로 배치 |          |
| `fixed`    |      브라우저 창을 기준으로 배치       |          |

| 값         |                     의미                     |   기본값 |
| ---------- | :------------------------------------------: | -------: |
| `static`   |        유형(기준) 없음 / 배치 불가능         | `static` |
| `relative` |        요소 **자신**을 기준으로 배치         |
| `absolute` | 위치 상 **_부모_(조상)요소**를 기준으로 배치 |
| `fixed`    |       **브라우저 창**을 기준으로 배치        |

# 6. 이미지 ( Image )

```
img , gif 파일들을 올려 활용 할 수 있습니다.

![대체 텍스트 ( alter text ) 입력 ]( http://~~~~~~~.jpg "링크 설명 ( 마우스 오버 했을 때 보이는 글씨" ))

![대체 텍스트][image name]

[image name]: http:~~~~~~~~~~~~~~.jpg "링크 설명"


```

```
원시 html 로 img 삽입

<img
  src="https://user-images.githubusercontent.com/32259122/75038657-2656c780-54fa-11ea-9a25-b837951dfa23.png"
width = 100px height - 100px>

width, height 등으로 크기 조절 가능
```

<img src = "https://user-images.githubusercontent.com/32259122/75038657-2656c780-54fa-11ea-9a25-b837951dfa23.png" width = 100px height = 100px>

# 각주

글에 세부 참조 사항을 달 수 있습니다.<sup>[1](#test)</sup>

<a name="test">1</a>: 각주에 관한 설명을 이러한 폼으로 작성하면 연결된 각주를 만들수 있습니다.
