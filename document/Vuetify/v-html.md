# HTML 코드를 직접 "template" 안에 넣을 수 있는 명령어 ( v-html )

v-html 은 HTML 코드를 직접적으로 입력해줄 때 사용되는 디렉티브 입니다.

data 내에 HTML 코드 자체가 선언되어 있을 때

```
"recipe": "<img src='http://www.foodsafetykorea.go.kr/uploadimg/cook/20_00017_1.png' /><p>1. 고구마는 깨끗이 씻어서 껍질을 벗기고 4cm 정도로 잘라준다.a</p><img src='http://www.foodsafetykorea.go.kr/uploadimg/cook/20_00017_2.png' /><p>2. 찜기에 고구마를 넣고 20~30분 정도 삶아 주고, 블렌더나 체를 이용하여 잘 으깨어 곱게 만든다.b</p><img src='http://www.foodsafetykorea.go.kr/uploadimg/cook/20_00017_3.png' /><p>3. 고구마와 물을 섞어 끓이면서 찹쌀가루로 농도를 맞추고 설탕을 넣어 맛을 낸다.c</p><p>4. 잣을 팬에 노릇하게 볶아 다져서 고구마 죽에 섞는다. 기호에 따라 고구마를 튀겨 얹어 먹어도 좋다.</p>"
```

이처럼 String 형태로 들어 있기 때문에 이를 View에서 보여주려면 split 함수 등으로
HTML 코드를 분석하여 입력해야하고 , 일정한 규격이 아니라면 분석 과정에서
일정하지 않은 결과가 도출 될 수 도 있습니다.

이럴 때 HTML 코드로 출력하기 위해서는 v-html 을 사용하면 용이하게 할 수 있습니다.

[HTML CODE]

```html
<div id="app">
  <p v-html="v_html_test"></p>
</div>
```

```javascript
new Vue({
  el: "#app",
  data: {
    v_html_test: "<a href='http://www.naver.com'>링크</a>",
  },
});
```

이처럼 v-html을 적용하게 되면 html String으로 온 데이터를 별도의 작업 없이도

html 코드 그대로 삽입하여 사용하는 것이 가능합니다.
