# HTML 4장
## 색상
- 140개의 표준 색상 이름 지원
- 배경색 `background-color`
- 글자 색깔 `color`
- 테두리 색깔 `border`
- 색상 값은 `#ffffff`, `rgb(0,0,0)`, `HSL(9, 100%, 64%)` 사용
- 색상과 투명도를 동시에 사용할 땐 `rgba`, `hsla`를 사용

## CSS
- Cascading Style Sheet
- 웹 페이지 레이아웃 서식
- 색상 `color`, 글꼴 `font-family`, 텍스트 크기 `font-size`, 간격 제어 `margin, padding`
- 요소 사이, 요소가 배치되는 방식, 배경 이미지
- 장치마다 다른 디스플레이 사용
- HTML요소 내부 속성에 사용, 섹션 요소에 사용 head 부분, 외부 css 파일 연결

## 링크
- 하이퍼링크
  + HTML 링크는 하이퍼링크
  + 링크를 클릭하고 다른 문서로 이동 가능
  + 링크는 꼭 텍스트일 필요 없음
- 구문
  + `<a>`
  + ```
    <a href="url">link text</a>
    ```
- 대상 속성
  + 링크된 페이지는 현재 브라우저 창에 표시됨
  + 이를 변경하기 위해서는 링크를 다른 대상에 지정
  +  `target`
  +  `_self` : 기본값에서 문서를 엶, 클릭한 것과 동일한 창/탭
  +  `_blank` : 새창 또는 탭에서 문서를 엶
  +  `_parent` : 상위 프레임에서 문서를 엶
  +  `_top` : 창의 전체 본문에서 문서를 엶
- 절대 URL vs 상대 URL
  + `href` 부분에 `"https://www"` 사용하면 절대, `/`를 사용하면 상대
- 이미지 링크
  + ```
    <a href="default.asp">
    <img src="smiley.gif" alt="HTML tutorial" style="width:42px;height:42px;">
    </a>
    ```
- 이메일 주소 링크
  + ```
    <a href="mailto:someone@example.com">Send email</a>
    ```
- 링크 버튼
  + ```
    <button onclick="document.location='default.asp'">HTML Tutorial</button>
    ```
- 링크 제목
  + ```
    <a href="https://www.w3schools.com/html/" title="Go to W3Schools HTML section">Visit our HTML Tutorial</a>
    ```
 - 링크 색상
   + ```
     <style>
     a:link {
       color: green;
       background-color: transparent;
       text-decoration: none;
     }
     
     a:visited {
       color: pink;
       background-color: transparent;
       text-decoration: none;
     }
     
     a:hover {
       color: red;
       background-color: transparent;
       text-decoration: underline;
     }
     
     a:active {
       color: yellow;
     background-color: transparent;
     text-decoration: underline;
     }
     </style>
     ```
 - 북마크
   + `id` 속성 이용
   + ```
     모두 같음
     <h2 id="C4">Chapter 4</h2>
     <a href="#C4">Jump to Chapter 4</a>
     <a href="html_demo.html#C4">Jump to Chapter 4</a>
     ```
