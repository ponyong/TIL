Vue에서 가장 많이 사용하는 HTTP 통신 **라이브러리**

CDN 방식, NPM 설치 방식 모두 지원하며 Promise 기반 코드를 작성하기 용이함.

CDN 방식

```html
<script src="https://unpkg.com/axios/dist/axios.min.js"></script>
```

NPM 방식

```html
npm install axios
```

import axios from "axios";

```
axios.get("url")
    .then(response) => {
        불러온 json 파일을 가공하는 단계
    }
    .catch(e) => {
        발생한 에러를 처리하는 단계
    }
```
