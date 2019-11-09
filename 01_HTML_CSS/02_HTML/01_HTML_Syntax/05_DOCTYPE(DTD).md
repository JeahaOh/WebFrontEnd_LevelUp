# HTML 문서의 범위
index.html 같은 HTML 파일을 우리는 HTML 문서라고 표현할 수 있음.  
HTML 문서의 범위를 나타내는(의미하는) 태그들.  
  
```
<!DOCTYPE html>
<html>
  <head>
    문서의 정보
  </head>
  <body>
    문서의 구조
  </body>
</html>
```
```
<!DOCTYPE html>
<html>
<head>
    <meta charset="UTF-8">
    <meta name="author" content="제하제하">
    <meta name="description" content="제하 열공!">
    <title> Studing HTML </title>
    <link rel="stylesheet" href="./css/main.css">
    <script src="./js/main.js"></script>
</head>
<body>
    <section>
      <h1></h1>
      <div>
        <ul>
          <li></li>
          <li></li>
        </ul>
      </div>
    </section>
</body>
</html>
```
  
## HTML(전체 범위)
`<html>`는 HTML 문서의 전체 범위를 지정.  
웹 브라우저가 해석해야 할 HTML 문서가 어디에서 시작하며, 어디에서 끝나는지 알려주는 역할.  
  
## HEAD(정보 범위)
웹 브라우저가 해석해야 할 HTML 문서의 정보 범위를 지정함.  
여기서 말하는 정보에는 웹 페이지의 제목, 웹 페이지의 문자 인코딩 방식, 연결할 외부 파일의 위치, 웹 페이지를 구조화하기 위한 기본 세팅 값 같은 것들을 의미.  
다르게는 ‘화면을 구성하기 위한 기본 설정’이라고 생각할 수 있음.  
  
## BODY(구조 범위)
웹 브라우저가 해석해야 할 HTML 문서의 구조 범위를 지정.  
구조는 사용자가 화면을 통해서 볼 수 있는 내용(콘텐츠)의 형태나 레이아웃 등을 의미,  
로고, 헤더, 푸터, 내비게이션, 메뉴, 버튼, 입력창, 팝업, 광고 등 보이는 모든 것들이 구조에 해당함.  
구조는 BODY 범위 안에서만 생성함.  
  
## DOCTYPE(DTD, 버전 지정)
DOCTYPE(DTD, Document Type Definition)은 마크업 언어에서 문서 형식을 정의함.  
이는 웹 브라우저에 우리가 제공할 HTML 문서를 어떤 HTML 버전의 해석 방식으로 구조화하면 되는지를 알려줌.  
(HTML은 크게 1, 2, 3, 4, X-, 5 버전이 있다)  
  
현재의 표준 모드는 HTML5.
```
<!-- HTML 5 -->
<!DOCTYPE html>

<!-- XHTML 1.0 Transitional -->
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
```
그 외 문서형 정보 : https://en.wikipedia.org/wiki/Document_type_declaration

