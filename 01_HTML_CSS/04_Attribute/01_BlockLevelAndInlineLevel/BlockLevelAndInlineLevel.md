# HTML - 블록 레벨(Bock Level) 요소와 인라인(Inline) 요소.
## 1. 블록 요소
  1. div, h, p
  2. 사용 가능한 최대 가로 너비를 사용한다.
  3. 크기를 지정할 수 있다.
  4. (width: 100%; height: 0;)이 기본 값이다.
  5. 기본적으로 수직으로 쌓인다.
  6. margin, padding 위, 아래, 좌, 우 사용 가능하다.
  7. 레이아웃 작성 용도

## 2. 인라인 요소
  1. span, img
  2. 필요한 만큼의 너비를 사용한다.
  3. 크기를 지정할 수 없다.
  4. (width: 0; height: 0;)이 기본값이다.
  5. 기본적으로 수평으로 쌓인다.
  6. margin, padding 위, 아래는 사용할 수 없다.
  7. TEXT 작성 용도.

```
기본적으로
  div { display: block; }
  h1 { display: block; }
  p { display: bock; }

  span { display: inline; }
```