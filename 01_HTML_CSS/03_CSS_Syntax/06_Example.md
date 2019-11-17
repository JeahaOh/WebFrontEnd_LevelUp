# CSS 예제
HTML 끝으로 작성했던 예제에 이어서 CSS를 적용해 봅시다.
`example1` 디렉터리 안에 `css`라는 이름의 디렉터리를 추가로 생성합니다.(Side bar 영역에서 우클릭 > 새폴더 선택)
생성한 `css` 디렉터리 안에 `main.css` 파일을 생성합니다.

다음은 이 예제의 디렉터리와 파일 구조입니다.
  
```
/example1
├─ /css
│  └─ main.css
└─ index.html
```
  
(아직 CSS 내용은 작성하지 않았지만) 생성한 `main.css` 파일은 기존의 `index.html` 파일과 연결해야 사용할 수 있습니다.
`<link>`를 이용해 HTML 외부에 존재하는 CSS 파일(방금 생성한 `main.css`)을 연결합니다.  
  
```
<head>
  <!-- 생략... -->
  <link rel="stylesheet" href="./css/main.css">
</head>
```
  
연결이 되었으니 CSS를 다음과 같이 작성합니다.  
```
body {
  /* 브라우저마다 기본 설정으로 BODY 요소에 margin과 padding의 값이 설정되어 있습니다. */
  /* 각각의 브라우저마다 BODY 요소가 다른 값을 가지고 있을 수 있으므로 우리가 일정하게 초기화해서 사용합니다. */
  /* 0은 단위를 사용하지 않습니다. */
  margin: 0;
  padding: 0;
}
.header {
  /* 화면에는 다음의 값으로 랜더링 되어 있는데 여러 이유로(설명이 많이 필요합니다) 생략 가능합니다. */
  /* width: 100%; */
  /* height: 75px; */
  background-color: white;
  border-bottom: 1px solid lightgray; /* 요소테두리선-아래: 1px두께 가는실선 밝은회색; - header 하단에 회색의 선이 표시됩니다. */
}
.container {
  /* height: 75px; */
  width: 980px;
  margin: auto; /* 요소바깥여백: 여백자동; - 이 속성과 값은 container를 수평 가운데 정렬하는 속성으로 쓰입니다. */
}
.container-left {
  /* width: 370px; */
  /* height: 75px; */
  /* float: left; */
  padding-top: 20px;
  padding-bottom: 20px;
}
.logo {
  margin-right: 5px;
  float: left; /* 수평정렬: 왼쪽부터차례대로; - logo와 menu를 수평 정렬하기 위해 사용되었습니다. 이 속성의 정확한 의미는 수평 정렬이 아니지만 쉽게 이해하도록 의역했습니다. */
}
.logo img { /* logo의 자식 요소인 img 태그 - 선택자에서 띄어쓰기는 자식요소를 의미합니다. */
  display: block; /* 요소특성: 형태위주; - img(이미지) 하단에 생기는 불필요한 여백을 없애기 위해서 사용되었습니다. */
}
.menu {
  float: left; /* logo와 menu를 수평 정렬하기 위해 사용되었습니다. */
}
.menu-item {
  font-size: 16px;
  padding: 8px 10px; /* padding-top: 8px; padding-bottom: 8px; padding-left: 10px; padding-right: 10px; 과 같습니다. */
  float: left; /* 각 menu-item들을 수평 정렬하기 위해 사용되었습니다. */
}

/* float: left; 를 사용하고 마무리할 때 필요한 코드입니다. */
/* float: left;를 사용한 해당 HTML 요소의 부모 요소에게 class="clearfix"를 입력하여 CSS float 속성에서 발생하는 현상을 해제합니다. */
.clearfix::after {
  content: "";
  display: block;
  clear: both;
}
```
큰 단위의 요소(`header`)부터 코딩하는 방법과, 작은 단위 요소(`menu-item`나 `logo`)부터 코딩하는 방법을 번갈아 가면서 하나하나 변화를 눈으로 익히며 연습을 하시면 금방 익숙해질 겁니다.

이 부분이 중요한데, `float: left`를 사용했다면 사용한 요소의 부모 요소에 꼭 `class="clearfix"`를 입력하고 변화를 확인하세요.(정확한 사용법과 의미는 상당한 분량이라서 여기서 설명하지 않겠습니다)
최종 HTML은 다음과 같습니다. 기존과 달라진 부분을 잘 살펴보세요.
```
<!DOCTYPE html>
<html>
<head>
    <meta charset="UTF-8">
    <title>GitHub</title>
    <!-- link 요소가 추가 되었군요! -->
    <link rel="stylesheet" href="./css/main.css">
</head>
<body>
    <div class="header">
        <!-- clearfix 클래스 값이 추가 되었군요! -->
        <!-- class 속성은 띄어쓰기로 여러 클래스를 구분하여 동시에 사용할 수 있습니다. -->
        <!-- 아래 요소는 <div class="container" class="clearfix"> 와 같습니다. -->
        <div class="container clearfix">
            <!-- clearfix 클래스 값이 추가 되었군요! -->
            <div class="container-left clearfix">
                <div class="logo">
                    <img src="https://heropcode.github.io/GitHub-Responsive/img/logo.svg" alt="GitHub Logo">
                </div>
                <!-- clearfix 클래스 값이 추가 되었군요! -->
                <div class="menu clearfix">
                    <div class="menu-item">Personal</div>
                    <div class="menu-item">Open Source</div>
                    <div class="menu-item">Business</div>
                    <div class="menu-item">Explore</div>
                </div>
            </div>
        </div>
    </div>
</body>
</html>
```
다음과 같은 결과가 나와야 합니다.

# 앞으로..
작성하다보니 입문자들의 이해를 돕기 위해 생략하거나 의역한 부분이 많습니다.  
하지만 시작이 반이라고 여기까지 오셨다면 충분히 성공하셨다고 생각합니다.  
많은 비전공 입문자가 생소한 학습 환경에 좌절하지만, HTML/CSS가 사실 그렇게 어려운 내용은 아닙니다.  
자신감을 가질 필요가 있습니다!  
  
자, 그러면 입문은 끝났고 앞으로는 어떻게 학습해야 하는지 간단히 정리하겠습니다.  
  
원하는(학습하고자 하는) HTML, CSS, JavaScript(ECMAScript, ES)의 내용을 검색할 때는 html div tag mdn 혹은 css background mdn과 같이 ‘MDN’를 함께 검색하세요.  
MDN 웹 문서는 모질라(파이어폭스 웹 브라우저)의 공식 웹사이트로 대부분의 문서에서 여러 설명과 예제 그리고 한글을 지원하며 매우 신뢰할 수 있습니다.  
W3C의 웹 표준 문서가 교과서라면 MDN은 해설집 정도로 이해하시면 쉽겠네요.  
  
또는 W3Schools 웹사이트도 추천합니다. MDN과 다르게 영리 목적(배너 광고 등)의 사이트이지만 입문자가 접하기에 좋게 잘 구성되어 있습니다. 단, 정보의 신뢰도는 MDN보다 떨어집니다.  
  
끝까지 읽어주셔서 감사하고, 이 포스트가 많은 입문자들에게 도움이 되길 희망합니다.  
