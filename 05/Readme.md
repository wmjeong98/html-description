# HTML 6장
## 블록 및 인라인 요소
- 일반적으로 사용되는 블록 요소 `<div>` `<p>`
- `<span>` 필요한 만큼만 너비를 차지하는 인라인 요소
- `<div>` 섹션 나눌 때 사용
- `<div>` 스타일에서 나란히 쓸 때 `float`는 여백 X, `display: inline-block`은 여백 O
- `flex`를 가장 많이 사용(반응형 레이아웃) `float` `position` 사용하지 않는 구조체
- `grid` : `flex`와 유사하지만 그리드 기반 레이아웃이며 1개 이상의 행을 정의해, 각 행의 위치를 개별적으로 지정할 수 있는 기능
- **블록 요소와 인라인 요소 차이점**
  + **블록 요소**
    - 블록 요소는 페이지의 구조를 형성하여 레이아웃을 정의
    - `vertical-align` `text-align` 적용 X
    - **모든 인라인 요소를 포함**할 수 있고 다른 **블록 요소도 일부 포함** 가능
    - 기본적으로 **가로폭 전체의 넓이를 가지는 직사각형 형태**
    - `width` `height` `margin` `padding` 로 레이아웃 수정 가능
    - **줄바꿈 O**
  + **인라인 요소**
    - 인라인 요소는 텍스트를 강조하거나 스타일을 적용하는 데 사용
    - `height` `width` 적용 X
## 클래스
- **여러 HTML 요소가 동일한 클래스 공유 가능**
- 클래스 이름 변환
- 특정 클래스 이름을 가진 요소 조작
- 자바스크립트 액세스 시 사용
- 클래스 이름은 대소문자 구분
- 모든 HTML 요소에서 사용 가능
- CSS 속성 정의 시 `.클래스이름 {}`으로 정의
- 여러 클래스 정의 시 공백으로 구분
  ```
  <h2 class="city main">London</h2>
  <h2 class="city">Paris</h2>
  <h2 class="city">Tokyo</h2>
  ```
- 서로 다른 HTML 요소가 같은 클래스 이름 가리킬 수 있음
  ```
  <h2 class="city">Paris</h2>
  <p class="city">Paris is the capital of France</p>
  ```
- 자바스크립트에서 클래스 속성 사용 `getElementsByClassName()`
  ```
  <script>
  function myFunction() {
    var x = document.getElementsByClassName("city");
    for (var i = 0; i < x.length; i++) {
      x[i].style.display = "none";
    }
  }
  </script>
  ```

## 아이디
- **동일한 아이디를 가진 요소를 두 개 이상 가질 수 없음**
- 고유 아이디 지정
- 특정 스타일 선언으로 변환 가능
- 자바스크립트 액세스 시 사용
- CSS 속성 정의 시 `#아이디이름 {}`으로 정의
- 아이디 이름은 대소문자 구분
- 
