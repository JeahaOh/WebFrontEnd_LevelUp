# 커리큘럼
[Content] : (https://heropy.blog/2019/04/24/html-css-starter/)  
입문자에게 추천하는 HTML, CSS 첫걸음.
  
# HTML, CSS, JS
- HTML  
- CSS  
- JS  
  
[TIP](https://html-css-js.com/)
  
# 웹 표준(Web Standard)
웹에서 사용되는 표준 기술이나 규칙.  
대부분의 경우 표준화 제정 단계의 ‘권고안(REC)’에 해당하는 기술을 표준이라고 생각하면 됨.  
  
# 크로스 브라우징
EX는 그만 서라 제발.  
  
# 웹 접근성
  
# Editor
VS Code.  
Web Storm.  
  
# VS Code 설치 및 설정
  
# 한글패치
Korean Language Pack for VS Code  
  
# Beautify & Live Server
## Beautify 설정
Beautify 설명의  
Commands에서  
HookyQR.beautify : Beautify Selection  
선택 영역에 대해서 포메팅을 하는 명령  
  
[Code] - [Preferences] - [Keyboard_Shortcuts](CMD + K + S)로 들어간 뒤 
검색에서 HookyQR.beautify 검색 단축키 설정 해 줌. (CMD + ALT + L)  
  
## Live Server
HTML파일 작성 할 때 VS Code Status Bar에서 Go Live 버튼 누르면 Live Server가 켜짐.  
한번 더 누르면 꺼짐.
  
# ETC Extension
- Terminal
- Live Sass Compiler
- Turbo Console log
- Better Comments
- High Light Matching Tag
- GitLens
- Rest Client
  
# Shortcut
`Preference > Keyboard Shortcut (CMD + K + S)`에서 단축키를 확인하거나 변경할 수 있다.  
명령 이름이나 키 바인딩(")으로 검색 할 수 있다.  
키바인딩으로 검색 시 `"cmd + control + alt` 와 같이 "를 닫지 않고 검색하는 것이 좋다.  

|       Windows 단축키       |        macOS 단축키        | 설명 |
|--------------------------|---------------------------|---|
|“Ctrl + B"                | "Cmd + B"                 | 사이드바 열기/닫기|
|“Ctrl + P"                | "Cmd + P"                 | 빠른 열기(파일이나 기호 탐색)|
|“Ctrl + Shift + P"        | "Cmd + Shift + P"         | 모든 명령 표시(에디터의 모든 명령에 접근)|
|“Ctrl + F"                | "Cmd + F"                 | 찾기(검색)|
|“Ctrl + H"                | "Cmd + Opt(Alt) + F"      | 찾기(검색)/바꾸기(대체)|
|“Alt + Up"                | "Alt + Up"                | 줄 위로 이동|
|“Alt + Down"              | "Alt + Down"              | 줄 아래로 이동|
|“Shift + Alt + UpArrow"   | "Shift + Alt + UpArrow"   | 위에 줄 복사|
|“Shift + Alt + DownArrow" | "Shift + Alt + DownArrow" | 아래 줄 복사|
|“Tab"                     | "Tab"                     | 들여쓰기|
|“Shift + Tab"             | "Shift + Tab"             | 내어쓰기|
|“Ctrl + PageUp"           | "Cmd + Shift + ["         | 이전 편집기 열기(좌측 창으로 전환)|
|“Ctrl + PageDown"         | "Cmd + Shift + ]"         | 다음 편집기 열기(우측 창으로 전환)|
|“Ctrl + \"                | "Cmd + \"                 | 편집기 분할(백슬래쉬)|
|“Ctrl + 숫자"              | "Cmd + 숫자"               | 숫자번째 분할된 편집기 그룹에 포커스|
|“Ctrl + W"                | "Cmd + W"                 | 편집기 닫기|
  
# 이미지에 대한 이해
## Bitmap And Vector
이미지(그래픽)는 크게 비트맵과 벡터로 구분됨.  

**비트맵(Bitmap)** 은 각 픽셀이 모여 만들어진 정보의 집합으로 레스터(Raster) 이미지라고도 함.  
픽셀 단위로 화면에 렌더링함. (렌더링: 컴퓨터가 화면에 그림을 그려서 우리가 볼 수 있게 하는것)  
우리가 일반적으로 사용하는 대부분의 이미지가 비트맵 형식임.  
그림판, 포토샵과 같은 툴로 편집할 수 있음.  
  
**벡터(Vector)** 는 수학적 정보의 형태(Shape)들이 만들어내는 결과물임.  
이미지가 가지고 있는 점, 선, 면의 위치(좌표), 색상 등의 정보를 온전히 가지고 있으며 그를 화면에 렌더링함.  
따라서 좀 더 많은 연산을 해야 하지만, 대신 해상도(픽셀)에 영향을 비트맵 이미지와 달리 해상도로부터 자유롭게 렌더링할 수 있음.  
쉽게 말하면 확대 및 축소를 해도 이미지가 깨지지 않음.  
또한 수학적 정보만을 가지고 있기 때문에 이미지 확대/축소에 따른 용량 변화가 없음.  
일러스트 같은 툴로 편집할 수 있음.  
  
- 비트맵 :  
  - 장점 : 정교함, 다양한 색을 자연스럽게 표현.
  - 단점 : 확대 / 축소 시 화질 떨어짐.
- 벡터 :  
  - 장점 : 확대 / 축소 시 화질 안떨어짐, 용량에 변화가 없음.
  - 단점 : 정교한 이미지(현실 사진)를 표현하기 어려움.
  
---
## JPG(JEPG)
JPG(Joint Photographic coding Experts Group) Foll-color와 Gray-scale의 압축을 위해 만들어 졌으며,  
압출률이 높아 사진이나 예술 분야에 많이 사용 됨.  
  
- 손실 압축
- 표현 색상도(24비트, 약 1600만 색상) 뛰어나 고해상도 표시장치에 적합
- **이미지의 품질과 용량을 쉽게 조절 가능**
- 가장 널리 쓰이는 이미지 포맷
  
---
## PNG
PNG(Portable Network Graphics)는 Gif의 대체 포맷으로 개발됨.  
  
- 비손실 압축
- 8비트(256 색상) / 24비트(약 1600만 색상) 컬러 이미지 처리
- Alpha Channel 지원(**투명도**)
- **W3C 권장 포맷**
  
---
## GIF
GIF(Graphics Interchange Format)는 이미지 파일 내에 이미지 및 문자열 같은 정보들을 저장할 수 있음.  
  
- 비손실 압축
- 여러 장의 이미지를 한 개의 파일에 담을 수 있음(**움짤**, 애니메이션)
- 8비트 컬러만 지원(다양한 색상을 표현하는 작업에는 적합하지 않음)
  
---
## WEBP
JPG, PNG, GIF를 모두 대체할 수 있는 구글이 개발한 이미지 포맷.  
  
- 완벽한 손실/비손실 압축 지원
- GIF 같은 애니메이션 지원
- Alpha Channel 지원(손실, 비손실 모두)
- 지원 브라우져가 거의 **없...**
  
---
## SVG
SVG(Scalable Vector Graphics)는 마크업 언어(HTML/XML) 기반의 벡터 그래픽을 표현하는 포맷.  
  
- 해상도의 영향에서 자유로움
- CSS로 Styling 가능
- JavaScript로 Event Handling 가능
- 코드 혹은 파일로 사용 가능
  
  
