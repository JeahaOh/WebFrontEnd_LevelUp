# CSS 선언 방식
이제 내가 작성한 CSS 코드를 어떻게 HTML에 적용할 수 있는지 알아보자.

## 태그에 직접 작성하기(인라인)
이 방법은 HTML 태그에 직접 작성하기 때문에 선택자가 필요하지 않음.

<div style="color: red;">태그에 직접 작성1</div> <!-- red -->
<div style="color: red;">태그에 직접 작성2</div> <!-- red -->
<div style="color: red;">태그에 직접 작성3</div> <!-- red -->
<div style="color: red;">태그에 직접 작성4</div> <!-- red -->

## HTML에 포함하기(내장)
CSS만 따로 작성하기 때문에 선택자가 필요함.
CSS 코드가 HTML의 `<style></style>` 안에 포함되어 있음.
```
<head>
  <style>
    div {
      color: red;
    }
  </style>  
</head>
<body>
  <div>HTML에 포함1</div> <!-- red -->
  <div>HTML에 포함2</div> <!-- red -->
  <div>HTML에 포함3</div> <!-- red -->
</body>
```
  
## HTML 외부에서 불러오기
CSS 코드를 완전히 분리할 수 있음.
분리된 하나의 CSS 파일을 여러 HTML 파일이 불러와서 사용할 수 있음.
```
<!-- HTML 1 -->
<head>
  <link rel="stylesheet" href="/css/main.css">
</head>
<body>
  <div>HTML에 외부에서 불러오기1</div> <!-- red -->
</body>
```
```
<!-- HTML 2 -->
<head>
  <link rel="stylesheet" href="/css/main.css">
</head>
<body>
  <div>HTML에 외부에서 불러오기2</div> <!-- red -->
</body>
```
```
/* main.css */
div {
  color: red;
}
```