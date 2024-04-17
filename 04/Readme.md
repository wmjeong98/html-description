# HTML 5장
## 이미지
- `<img>`
- `<src>` 이미지 경로, `<alt>` 이미지 대체 텍스트
- `style="width:?px;height:?px"` 너비와 높이 정의
- gif도 사용 가능
- 이미지 안에 링크 넣기
  + ```
    <a href="default.asp">
      <img src="smiley.gif" alt="HTML tutorial" style="width:42px;height:42px;">
    </a>
    ```
- `float` 좌/우에 이미지 띄우기
  + ```
    <p><img src="smiley.gif" alt="Smiley face" style="float:right;width:42px;height:42px;">
    The image will float to the right of the text.</p>
    
    <p><img src="smiley.gif" alt="Smiley face" style="float:left;width:42px;height:42px;">
    The image will float to the left of the text.</p>
    ``` 
- 이미지 맵 `<map>` 에서 클릭 가능한 영역 `<area>`
  + ```
    <img src="workplace.jpg" alt="Workplace" usemap="#workmap">
  
    <map name="workmap">
      <area shape="rect" coords="34,44,270,350" alt="Computer" href="computer.htm">
      <area shape="rect" coords="290,172,333,250" alt="Phone" href="phone.htm">
      <area shape="circle" coords="337,300,44" alt="Coffee" href="coffee.htm">
    </map>
    ```
- 배경으로 이미지 가능 `background-image`
- body에 배경으로 사용할 때 이미지가 작으면 수평 수직으로 채울때까지 반복
- 반복하기 싫으면 `background-repeat: no-repeat;` 사용
- 전체 요소를 덮도록 하려면 `background-size: cover;`
- 전체 요소가 항상 포함되도록 하려면 `background-attachment: fixed;`
- 배경 이미지가 전체 요소에 맞게 늘어나도록 하려면 `background-size: 100% 100%;`
- `<picture>` 화면 크기에 대해 다른 이미지 표시
  + ```
    <picture>
      <source media="(min-width: 650px)" srcset="img_food.jpg">
      <source media="(min-width: 465px)" srcset="img_car.jpg">
      <img src="img_girl.jpg">
    </picture>
    ```
  + `<source>` 에서 첫 번째 요소만 사용하고 나머지 요소는 무시
  + 일부 브라우저 또는 장치는 모든 이미지 형식을 지원하지 않을 수 있음
  + 그래서 브라우저는 첫 번째로 인식하는 형식을 사용함
- `<link rel="icon" type="image/x-icon" href="/images/favicon.ico">`
- 이용하면 title에 이미지 표시

## 테이블
- `<table> </table>` 안에 요소 추가
- `<th> </th>` 테이블 헤더, 나눌 요소들의 키워드
- `<tr> </tr>` 테이블 행
- `<td> </td>` 테이블 행 안에 들어갈 내용
- `border` 로 테두리 표현
- `border-collapse: collapse;`로 단일 테두리 표시
- 테이블 크기는 `width, height`로 지정
- 테이블 열 너비는 `th` 부분에 `width` 값을 넣어주면 됨
- 테이블 행 높이는 `tr` 부분에 `height` 값을 넣어주면 됨
- 수직 테이블 사용하고 싶으면 `<tr>` 안에 `<th> <td>`를 넣어주면 됨
- 테이블 제목 `<table>` 밑에 `<caption>제목</caption>` 작성
- 셀 병합 `<th colspan="2">` 이런 식으로 사용 //행 부분
- 셀 병합 `<th rowspan="2">` 이런 식으로 사용 //열 부분
- 테이블 가로 줄무늬 효과
  ```
  tr:nth-child(even or odd) {
    background-color: #D6EEEE;
  }
  ```
- 테이블 세로 줄무늬 효과
  ```
  th:nth-child(even or odd), td:nth-child(even or odd) {
    background-color: #D6EEEE;
  }
  ```
- 테이블 행 아래에만 가로 구분선
  ```
  tr {
    border-bottom: 1px solid #ddd;
  }
  ```
- 테이블 커서 올리면 강조 표시
  ```
  tr:hover {background-color: #D6EEEE;}
  ```
- 테이블 콜 그룹 `<colgroup> </colgroup>`
- `<col>` 각 콜 그룹 요소 `span` 스타일을 가져오는 열의 수 `style` 열 특성에 제공할 스타일
- 다중 col 요소도 가능
  ```
  <colgroup>
    <col span="2" style="background-color: #D6EEEE">
    <col span="3" style="background-color: pink">
  </colgroup>
  ```
- 스타일을 안주면 빈 col 요소도 가능
- `"visibility: collapse"` 열 숨기기

## 리스트
- 보통 `<ul>` `<li>` 태그 사용
  ```
  <ul>
    <li>Coffee</li>
    <li>Tea</li>
    <li>Milk</li>
  </ul>
  ```
- 순서 지정 리스트 `<ol>` `<li>` 태그 사용 `<ol>`에 type 정하면 숫자, 알파벳, 로마숫자 등으로 표시 가능
  ```
  <ol type="1">
    <li>Coffee</li>
    <li>Tea</li>
    <li>Milk</li>
  </ol>
  ```
- 설명 리스트 `<dl>` `<dt>` `<dd>` 태그 사용
  ```
  <dl>
    <dt>Coffee</dt>
    <dd>- black hot drink</dd>
    <dt>Milk</dt>
    <dd>- white cold drink</dd>
  </dl>
  ```
- 리스트 마크 표시 `list-style-type` 사용하고 기본값은 `disc`, 그 외에 `circle` `square` `none`
- 중첩 리스트 가능
- 리스트를 지정된 숫자부터 카운트 가능 `start` 속성 이용
  ```
  <ol start="50">
    <li>Coffee</li>
    <li>Tea</li>
    <li>Milk</li>
  </ol>
  ```
