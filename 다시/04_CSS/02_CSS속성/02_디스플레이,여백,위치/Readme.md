# 디스플레이
- ## `inline`
  - content 만큼의 크기를 가짐
  - 요소가 줄바꿈 없이 다른 요소와 같은 줄에 배치
  - `width height margin float` 설정 X
- ## `block`
  - `height`는 content 만큼의 크기를 갖지만, `width`는 부모 요소 `width`의 100%를 기본으로 갖는다
  - 요소가 줄바꿈되어 다른 요소가 있는 다음 줄에 배치
  - `width height margin float` 설정 O
- ## `inline-block`
  - `inline` `block`의 특성을 동시에 가짐
  - `inline`의 줄바꿈 없이 같은 줄 배치 + `block`의 크기 여백 설정

![디스플레이 속성값](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2F0WTom%2FbtrSL0lEpPT%2FlCXP0cZ79YCgQ8k0OSr6n0%2Fimg.jpg)
- ## `none`
  - 요소를 렌더링 하지 않게 하여 아예 보이지 않도록 설정
  - 화면에서 요소를 숨기고 공간을 차지하지 않게 함
  - 화면에서 요소를 숨기지만 공간이 남는 속성은 `visibility:hidden;`

![디스플레이 none](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FS9MlV%2FbtrSJTm52xr%2FaFrBgCSdmQPDMyM10FfdGk%2Fimg.jpg)

# 여백
- ## 속성값
    - 1개 : 상하좌우
    - 2개 : 상하/좌우
    - 3개 : 상/좌우/하
    - 4개 : 상/우/하/좌
- ## `padding`
  - border **안쪽** 여백
  - px, pt, cm, %
- ## `margin`
  - border **바깥쪽** 여백
  - auto, px, pt, cm, %, **margin:0 auto (중앙정렬)**

# 위치
- ## position
- ### `static`
  - 작성된 순서 그대로 원래 있어야 할 자기 자리에 위치
  - `top, right, bottom, left, z-index` 값을 주어도 무시

![static](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FbdFahe%2FbtrS5NNujtS%2FHlfIgTyJkYaMmLiiBbcavK%2Fimg.jpg)
  - ### `relative`
    - 원래 있던 자리에서 `top, right, bottom, left` 값에 따라 배치
    - 다른 요소에 영향을 주지않고, 원래 있던 자리는 그대로 유지

![relative](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FrTTdM%2FbtrS3pmAtLQ%2FyuCtEjHtGLMcALr1R4cG5k%2Fimg.jpg)
  - ### `absolute`
    - 기본적인 html 흐름에서 벗어나 원래 있던 자리가 없어짐
    - 부모요소를 기준으로 `top, right, bottom, left` 값에 위치

![absolute](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2F2Ix0e%2FbtrS43DwYLc%2FrBvs8ynURnZUc18tYNSg2K%2Fimg.jpg)
  - ### `fixed`
    - 기본적인 html 흐름에서 벗어나 원래 있던 자리가 없어짐
    - 뷰포트(브라우저 화면) 기준으로 설정한 `top, right, bottom, left` 값에 위치
    - 스크롤과 상관없이 화면에서 고정된 위치에 배치할 때 사용

![fixed](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FbhPDAp%2FbtrS6YgDRIL%2FLZxG6mNgU4gJ62O9qtABDK%2Fimg.jpg)
  - ### `sticky`
    - 다른 요소에 영향을 주지않고, 원래 있던 자리는 그대로 유지
    - 부모 요소가 스크롤 뒤어 뷰포트 기준으로 설정한 해당 요소의 위치값에 도달하면 `fixed` 처럼 위치에 고정됨
    - 해당 요소의 위치 값에 도달하기 전이나 부모 요소가 뷰포트에서 벗어난 후에는 `static` 처럼 원래 자기 자리에 위치
    - 부모 요소에 `overflow: hidden|scroll|auto;` 가 설정되어 있으면 `sticky` 작동 X
    - 부모 요소에 `height` 값 반드시 설
- ## `float`
- 왼쪽이나 오른쪽 구석에 요소를 배치시키는 기능
- `none left right`
- float 속성을 준 부모 요소는 높이 값을 잃어 자식 요소를 포함 못함 -> `overflow:hidden;` 으로 해결
- float는 상속이 되어서 다음 요소에 영향을 미침 -> `clear` 속성 이용
  - `clear` 속성값
    - `none` 요소가 어느쪽이든 float 가능
    - `left` 왼쪽에 float한 요소 뒤를 초기화
    - `right` 오른쪽에 float한 요소 뒤를 초기화
    - `both` 왼쪽, 오른쪽에 float한 요소 뒤를 초기화
