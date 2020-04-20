```html
<v-img src="url" width="가로 크기" height="세로크기"> </v-img>
```

| 변수명       |    디폴트 값    |             타입 | 뜻                                                                        |
| ------------ | :-------------: | ---------------: | ------------------------------------------------------------------------- |
| alt          |    undefined    |           string | image가 렌더링 되지 못했을 때 나타낼 문자열을 위한 값<sup>[1](#alt)</sup> |
| aspect-ratio |    undefined    |  number / string |                                                                           |
| contain      |      false      |          boolean |                                                                           |
| eager        |      false      |          boolean |                                                                           |
| gradient     |    undefined    |           string |                                                                           |
| height       |    undefined    |           string |                                                                           |
| width        |    undefined    |           string |                                                                           |
| max-height   |    undefined    |  number / string |                                                                           |
| max-width    |    undefined    |  number / string |                                                                           |
| min-height   |    undefined    |  number / string |                                                                           |
| min-width    |    undefined    |  number / string |                                                                           |
| options      |       {}        |           object |                                                                           |
| position     | 'center center' |           string |                                                                           |
| src          |    undefined    |  string / object |                                                                           |
| srcset       |    undefined    |           string |                                                                           |
| lazy-src     |    undefined    |           string |                                                                           |
| sizes        |    undefined    |           string |                                                                           |
| transition   | fade-transition | boolean / string |                                                                           |

<!-- 글 뒷 부분에 -->

<a name="alt">1</a>: 제한적인 환경에서 그림없이 문자열만 보여주는 경우 , 시각장애인을 위한 문서의 내용을 목소리를 변환시켜주는 음성합성 기술 등에 사용된다.
