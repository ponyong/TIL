```html
<v-img src="url" width="가로 크기" height="세로크기"> </v-img>
```

| 변수명       |    디폴트 값    |             타입 | 뜻                                                                                      |
| ------------ | :-------------: | ---------------: | --------------------------------------------------------------------------------------- |
| alt          |    undefined    |           string | image가 렌더링 되지 못했을 때 나타낼 문자열을 위한 값<sup>[1](#alt)</sup>               |
| aspect-ratio |    undefined    |  number / string | 화면 비율을 나타낸다 너비/높이로 나타낸다.<sup>[2](#aspect-ratio)</sup>                 |
| contain      |      false      |          boolean | 이미지가 맞지 않으면 이미지가 잘리지 않도록 방지                                        |
| eager        |      false      |          boolean |                                                                                         |
| gradient     |    undefined    |           string | 이미지에 간단한 그라데이션 오버레이를 적용 할 수 있습니다.                              |
| height       |    undefined    |           string | 컴포넌트의 높이를 설정합니다.                                                           |
| width        |    undefined    |           string | 컴포넌트의 너비를 설정합니다.                                                           |
| max-height   |    undefined    |  number / string | 컴포넌트의 최대 높이를 설정합니다.                                                      |
| max-width    |    undefined    |  number / string | 컴포넌트의 최대 너비를 설정합니다.                                                      |
| min-height   |    undefined    |  number / string | 컴포넌트의 최소 높이를 설정합니다.                                                      |
| min-width    |    undefined    |  number / string | 컴포넌트의 최소 너비를 설정합니다.                                                      |
| options      |       {}        |           object |                                                                                         |
| position     | 'center center' |           string |                                                                                         |
| src          |    undefined    |  string / object | 이미지의 URL / 필수요소                                                                 |
| srcset       |    undefined    |           string | 이미지 URL의 SET , 쉼표로 구분하는 한개 이상의 문자열입니다.                            |
| lazy-src     |    undefined    |           string | 메인 이미지가 로드 되기전 기다리는 동안 보여주는 이미지입니다.<sup>[3](#lazy-src)</sup> |
| sizes        |    undefined    |           string |                                                                                         |
| transition   | fade-transition | boolean / string |                                                                                         |

<!-- 글 뒷 부분에 -->

<a name="alt">1</a>: 제한적인 환경에서 그림없이 문자열만 보여주는 경우 , 시각장애인을 위한 문서의 내용을 목소리를 변환시켜주는 음성합성 기술 등에 사용된다.
<a name="aspect-ratio">2</a> 1920x1080 이미지 비율은 1.7778이 된다. 생략할 경우 자동으로 계산된다.
<a name="lazy-src">3</a> 일반적으로 base64로 인코딩된 작은 축소판 그림. 약간 흐릿한 필터가 적용되어 있다.
