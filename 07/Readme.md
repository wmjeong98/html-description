# HTML 7장
## `<form>`
- 사용자 입력을 수집하는 데 사용
- 대부분 처리를 위해 서버로 전송됨
- `<form>` 다양한 입력 요소에 대한 컨테이너
- `text fields checkbox radio button submit button` 등
  ```
  <form>
    <label for="fname">First name:</label><br>
    <input type="text" id="fname" name="fname"><br>
    <label for="lname">Last name:</label><br>
    <input type="text" id="lname" name="lname">
  </form>
  ```
- `<label>` 많은 레이블 정의
- 스크린 리더기가 레이블을 소리내어 읽음
- 입력 요소에 초점을 맞춤
- 라디오 버튼 같은 작은 영역에도 도움됨 -> 텍스트를 클릭하면 전환되기 때문
- `action` 속성 : 사용자가 버튼 등을 클릭할 때 서버의 파일로 전송 // 속성을 생략하면 작업이 현재 페이지로 설정 `<form action="/action_page.php">`
- `target` 속성 : 다음을 수행할 위치 지정, form을 제출하고 받은 응답을 표시 기본값은 `_self` `<form action="/action_page.php" target="_blank">`
- `method` 속성 : HTTP form 데이터를 제출할 때 사용할 방법 `GET` 과 `POST` 둘의 차이는 폼 데이터를 url에 (get)추가되느냐 (post)아니냐
- ```
  <form action="/action_page.php" method="get">
  <form action="/action_page.php" method="post">
  ```
- `autocomplete` 속성 : 자동완성기능 `on, off` 사용`<form action="/action_page.php" autocomplete="on">`
- `novalidate` 속성 : 유효성 검사하지 않도록 지정 `<form action="/action_page.php" novalidate>`
### `<form>` 요소
- `<input>`
  + 가장 많이 사용되는 요소
  + `type, id, name` 등 사용
- `<label>`
  + `for` 사용 다른 요소의 `id`와 동일
- `<select>`
  + 드롭다운 리스트 정의 `id name` 사용
  + `selected` 기본값으로 선택되는 첫번째 항목
  + `size` 표시되는 값의 수 지정
  + `multiple` 둘 이상의 값 선택 가능
- `<textarea>`
  + 메모장 같은 역할 텍스트 영역을 정의 `name` 사용
- `<button>`
  + 말 그대로 버튼, `type` 사용
  + 팝업창 등 클릭이벤트 `onclick` 사용
- `<fieldset>`
  + 관련 데이터 그룹화
- `<legend>`
  + `<fieldset>`의 캡션 정의
- `<datalist>`
  + `<input list>`를 이용하며 그 밑에 `<datalist id>`로 미리 정의된 드롭다운 리스트 확인 가능
    ```
    <form action="/action_page.php">
      <input list="browsers">
      <datalist id="browsers">
        <option value="Edge">
        <option value="Firefox">
        <option value="Chrome">
        <option value="Opera">
        <option value="Safari">
      </datalist>
    </form>
    ```
    +
- `<output>`
  + 계산 결과 요소
    ```
    <form action="/action_page.php"
      oninput="x.value=parseInt(a.value)+parseInt(b.value)">
      0
      <input type="range"  id="a" name="a" value="50">
      100 +
      <input type="number" id="b" name="b" value="50">
      =
      <output name="x" for="a b"></output>
      <br><br>
      <input type="submit">
    </form>
    ```
- `<option>`
  + `<select> <datalist>` 요소에서 리스트 항목 정의 `value` 사용
- `<optgroup>`
  + `<option>` 그룹화, 그룹화 할 때 `label` 사용
 
## `<input>` 종류
- `<input type="button">`
- `<input type="checkbox">`
- `<input type="color">`
- `<input type="date">`
- `<input type="datetime-local">`
- `<input type="email">`
- `<input type="file">`
- `<input type="hidden">`
- `<input type="image">`
- `<input type="month">`
- `<input type="number">`
- `<input type="password">`
- `<input type="radio">`
- `<input type="range">`
- `<input type="reset">`
- `<input type="search">`
- `<input type="submit">`
- `<input type="tel">`
- `<input type="text">`
- `<input type="time">`
- `<input type="url">`
- `<input type="week">`

## `<input>` 속성
- `value` : 초기 값
- `readonly` : 읽기 전용
- `disabled` : 필드 비활성화
- `size` : 너비, 기본값 20
- `maxlength` : 최대 문자 수
- `min max` : 최소값, 최대값
- `multiple` : 둘 이상의 값 입력하도록 지정
- `pattern` : 정규식 `pattern="[A-Za-z]{3}"` `pattern="[0-9]{3}-[0-9]{2}-[0-9]{3}"`
- `required` : 입력 필드 채워야 함
- `step` : 숫자 n에 대한 등차수열 숫자, 범위, 날짜 등에 쓰이고 `max, min`이랑 쓰면 올바른 값의 범위 만들기 가능
- `autofocus` : 페이지 로드 시 입력 필드 자동 포커스 -> 바로 입력 가능하게 됨
- `width height` : 너비 높이, 이미지에 사용
- `list` : 미리 정의된 옵션을 포함하는 요소 참조
- `autocomplete` : 자동완성
