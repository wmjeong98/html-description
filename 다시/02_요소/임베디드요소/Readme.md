# `<embed>`
- 여러가지 동영상, 음악, 플래시 관련 파일을 재생할 수 있는 태그
- `src` : 포함된 리소스 URL
- `width height`
- `hidden` : 콘텐츠 숨기기
- `loop`: 반복
# `<iframe>`
- 인라인 프레임, 해당 웹 페이지 안에 다른 html 파일을 불러와서 삽입할 수 있는 기능 제공 태그
- `width height`
- `src` : html 주소
- `name` : `iframe`요소 이름
- `sandbox` : `iframe` 요소에 보일 콘텐츠에 대한 추가 제한 사항 집합 명시
- `srcdoc` : `iframe` 요소에 보일 웹 페이지의 html 코드 명시
# `<object>`
- 이미지나 중첩 브라우저, 플러그인에 의해 다뤄질 수 있는 리소스와 같은 외부 리소스 나타냄
- `type` : 콘텐츠 타입
- `data` : 리소스 URL
- `width height`
# `<picture>`
- 0개 이상의 `<source>` 요소와 1개 이상의 `<img>` 요소가 포함된 디스플레이 에 대한 이미지 제공
# `<source>`
- 미디어 리소스 지정, 빈 요소
- `type` : 미디어 유형
- `src` : 리소스 URL
