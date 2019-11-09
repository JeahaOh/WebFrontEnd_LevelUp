# HTML 문서의 정보
`<head></head>` 안에서 사용하는 태그들은 HTML 문서의 정보를 가지고 있음.
  
---
## TITLE(웹 페이지의 제목)
HTML 문서의 제목을 정의함.  
웹 브라우저의 각 사이트 탭에서 이름으로 표시됨.  
구조보다는 정보를 나타낸다고 생각하면 됨.  
  
```
<head>
  <title>제하 제하</title>
</head>
```
  
---
## META(웹 페이지의 정보)
기타 모든 정보를 표현.  
HTML 문서(웹페이지)에 관한 정보(표시 방식, 제작자(소유자), 내용, 키워드 등)를 검색엔진이나 브라우저에 제공함.  
빈(Empty) 태그임.  
```
<head>
  <meta charset="UTF-8">
  <meta name="author" content="제하 제하">
  <meta name="description" content="제하 열공!">
</head>

<!-- 다음과 같이 이해할 수 있음. -->
<문서의정보범위>
  <정보 문자인코딩방식="UTF-8">   -> 필수
  <정보 정보종류="사이트제작자" 정보값="제하 제하">
  <정보 정보종류="사이트설명" 정보값="제하 열공!">
</문서의정보범위>
```
`<meta>`에서 사용할 수 있는 속성은 다음과 같음.  
각 태그는 자신이 사용할 수 있는 속성과 값이 정해져 있음.  
어떤 속성을 사용할 수 있고, 사용할 수 없는지 구분할 수 있어야 함.  
잘 사용하지 않는 속성도 있기 때문에 당장 모든 속성과 값을 암기할 필요는 없음.  
(‘전역(Global) 속성’이라고 해서 어느 태그에서나 사용할 수 있는 속성들도 있음만 지금은 확인할 필요가 없음.)  
  

| 속성      |   의미                                    | 값 |
|----------|------------------------------------------|---|
|`charset` | 문자인코딩 방식                              | `UTF-8`, `EUC-KR` 등.. |
|`name`    | 검색엔진 등에 제공하기 위한 정보의 종류(메타 데이터) | `author`, `description`, `keywords`, `viewport` 등.. |
|`content` | `name` 이나 `http-equiv` 속성의 값을 제공      |
  
---
## LINK(CSS 불러오기)
외부 문서를 연결할 때 사용함.  
특히 HTML 외부에서 작성된 CSS 문서(`xxx.css` 파일)를 불러와 연결할 때 사용함.  
빈(Empty) 태그임.  
```
<head>
  <link rel="stylesheet" href="./css/main.css">
  <link rel="icon" href="./favicon.png">
</head>

<!-- 다음과 같이 이해할 수 있음. -->
<문서의정보범위>
  <외부문서연결 관계="CSS" 문서경로="./css/main.css">
  <외부문서연결 관계="사이트대표아이콘" 문서경로="./favicon.png">
</문서의정보범위>
```
|속성 | 의미                               | 값 |
|----|-----------------------------------|---|
|rel | (**필수**)현재 문서와 외부 문서와의 관계를 지정 | `stylesheet`, `icon` 등..|
|href| 외부 문서의 위치를 지정                 |경로 |
  
---
## STYLE(CSS 작성하기)
CSS를 외부 문서에서 작성하여 연결하는 것이 아니고 HTML 문서 내부에 작성할 때 사용함.  
  
```
<style>
  img {
    width: 100px;
    height: 200px;
  }
  p {
    font-size: 20px;
    font-weight: bold;
  }
</style>

<!-- 다음과 같이 이해할 수 있음. -->
<스타일정의>
  <!-- CSS 코드 -->
</스타일정의>
```
  
---
## SCRIPT(JS 불러오거나 작성하기)
HTML 문서에서 CSS는, 작성된 CSS를 `<link>`로 불러오거나 `<style></style>`안에 작성할 수 있음.   
JS는 `<script></script>`로 이 2가지 방식을 모두 사용할 수 있음.  
  
```
<!-- 불러오기 -->
<script src="./js/main.js"></script>

<!-- 작성하기 -->
<script>
  function windowOnClickHandler(event) {
    console.log(event);
  }
  window.addEventListener('click', windowOnClickHandler);
</script>

<!-- 다음과 같이 이해할 수 있음. -->

<!-- 불러오기 -->
<자바스크립트 문서경로="./js/main.js"></자바스크립트>

<!-- 작성하기 -->
<자바스크립트>
  <!-- JS 코드 -->
</자바스크립트>
```