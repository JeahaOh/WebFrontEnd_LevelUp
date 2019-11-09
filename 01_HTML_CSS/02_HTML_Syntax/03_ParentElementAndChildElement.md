# 부모와 자식 요소
태그A가 태그B의 콘텐츠로 사용되면, 태그B는 태그A의 부모 요소, 태그A는 태그B의 자식 요소라고 합.

```
<PARENT>
  <CHILD></CHILD>
</PARENT>
```
```
<section class="fruits">
  <h1>과일 목록</h1>
  <ul>
    <li>사과</li>
    <li>딸기</li>
    <li>바나나</li>
    <li>오렌지</li>
  </ul>
</section>

<!-- 다음과 같이 이해할 수 있음. -->
<섹션영역 태그별명="fruits">
  <주제1>과일 목록</주제1>
  <순서없는목록>
    <항목>사과</항목>
    <항목>딸기</항목>
    <항목>바나나</항목>
    <항목>오렌지</항목>
  </순서없는목록>
</섹션영역>
```
`<section></section>` 안에는(콘텐츠) `<h1></h1>`, `<ul></ul>`, `<li></li>`가 있고,  
`<ul></ul>` 안에는(콘텐츠) `<li></li>`가 있음.  
이러한 구조에서 `<section>`는 `<h1>`과 `<ul>`의 부모 요소임.  
또한 `<ul>`은 `<li>`의 부모 요소임.  
반대로 `<h1>`과 `<ul>`은 `<section>`의 자식 요소임.  
또한 `<li>`는 `<ul>`의 자식 요소입니다.  
  
여기서 `<ul>`은 `<section>`의 자식 요소이면서 `<li>`의 부모 요소임.  
이처럼 부모와 자식 요소는 상대적인 개념임.  
(조금 더 나아가면 `<section>`은 `<li>`의 조상(상위) 요소, 반대로 `<li>`는 `<section>`의 후손(하위) 요소라고 함.)  
  
우리가 기본적인 가계도를 통해 할아버지, 엄마, 삼촌, 형제 같은 호칭을 정의하듯(혹은 반대로 호칭을 통해 가계도를 이해하듯),  
HTML의 구조도 위와 같은 개념으로 호칭을 정의하여 추후 선택자(Selector)를 통해 CSS와 JS로 HTML을 다룰 때 중요하게 사용됨.  