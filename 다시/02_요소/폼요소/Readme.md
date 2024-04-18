# `<button>`
- 클릭 가능 버튼
- `disabled` : 모든 자손 컨트롤 비활성화
- type 속성 : `button`, `submit`, `reset`
# `<datalist>`
- 다른 컨트롤에서 고를 수 있는 선택지를 나타내는 옵션 요소를 담는 데이터리스트
# `<fieldset>`
- 웹 양식의 여러 레이블 묶을 때 사용
- `disabled` : 모든 자손 컨트롤 비활성화
# `<form>`
- 정보 제출을 위한 대화형 컨트롤을 포함하는 문서 구획
- `action` : 데이터 처리할 프로그램의 특성
- `method` : 양식 제출용 메소드 `get` `post` 사용
- `target` : 양식 제출 결과 표시창
# `<label>`
- 사용자 인터페이스 항목의 설명
- 라디오 버튼, 체크박스 등의 설명
# `<legend>`
- 부모 `<fieldset>` 콘텐츠의 제
# `<meter>`
- 특정 범위 내 스칼라 값, 백분율 값
- `value` : 현재 값
- `min max` : 측정 범위 최소/최대값
- `low` : 측정 범위 중 낮은 범위의 최소값
- `high` : 측정 범위 중 높은 범위의 최대값
- `optimum` : 이상적인 값
- `id`
# `<optgroup>`
- `<select>` 요소의 옵션을 묶음
- `disabled` : 하위 옵션 선택 불가능
- `label` : 옵션 그룹 이름, 필수 지정
# `<option>`
- `<select> <optgroup> <datalist>` 요소의 항목을 정의
- `value` : 데이터값
- `selected` : 초기에 선택되어있는 항목
- `disabled` : 옵션 선택 불가능
- `label` : 옵션의 의미를 나타내는 텍스트
# `<output>`
- 계산 결과
- `for` : 스페이스로 구분한 다른 여러 요소 `id`의 목록
- `name` : 요소 이름
# `<progress>`
- 작업 완료 정도, 진행 표시줄
- `max` : 작업량, 기본값 1
- `value` : 작업을 완료한 양
# `<select>`
- 옵션 메뉴를 제공하는 컨트롤
- `multiple` :  중복 선택
- `required` : 비어 있지 않은 문자열 값 옵션 선택 Boolean값
# `<textarea>`
- 메모장 역할 수행하는 컨트롤
- `cols rows` : 행렬 수
- `name` : 컨트롤 이름
- `minlength maxlength` : 최대/최소 문자열 길이
- `required` : 양식 제출 전 값을 입력해야함
# `<input>`
- 입력식 대화형 컨트롤 생성
- ## `<input>` 종류
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

- ## `<input>` 속성
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
