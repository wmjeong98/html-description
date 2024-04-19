# Grid

![Grid Layout](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2F6MyfX%2Fbtrg0pxkTXp%2FSKZAJzQO1U0GlzxB4mqeBK%2Fimg.png)

- ## Grid container
  - `display`에 `grid`를 설정하며 모든 그리드 아이템의 부모 요소
- ## Grid items
  - 그리드 컨테이너의 자식 요소
- ## Grid line
  - 그리드를 구성하는 분할 선
- ## Grid track
  - 두 개의 그리드 라인 사이의 공간. 열 또는 행
- ## Grid cell
  - 그리드 구성 단위
- ## Grid area
  - 네 개의 그리드 라인으로 둘러싸인 공간. N개의 그리드 셀로 구성
- ## Grid number
  - 그리드 라인의 각 번호
- ## Grid gap
  - 그리드 셀 사이의 간격
- ## Grid container 속성
  - ### `display`
    - 컨테이너 정의
    - `grid, inline-grid`
  - ### `grid-template-rows` `grid-template-columns`
    - 행/열의 트랙 기준으로 크기와 갯수를 정함 (col 가로 길이, row 세로 길이)
    - `단위, repeat(반복횟수, 크기), repeat(반복횟수, minmax(최소크기, 최대크기)), repeat(auto-fill, 크기)`
       `repeat(auto-fit, 크기)`
  - ### `grid-template-areas`
    - 지정된 그리드 영역 이름을 참조해 템플릿 생성
    - ```
      grid-template-areas:
      "header header header"
      "main   main   aside"
      "footer footer footer";
      ```
     ![그리드1](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FbwihkI%2Fbtrg3q2IS3Z%2FTg6ZpDvnf1nZaIjgycU7z0%2Fimg.png)
      ```
      grid-template-areas:
      "header header header"
      "main     .      .   "
      "main     .    aside "
      "footer footer footer";
      ```
      ![그리드2](https://blog.kakaocdn.net/dn/yu6xp/btrg0pxkTZD/xKrnB1NB0ZAznvA2prBzFK/img.png)
  - ### `grid-template`
    - `grid-template-rows` `grid-template-columns` `grid-template-areas`의 단축 속성
  - ### `grid-auto-rows` `grid-auto-columns`
    - 만들고자 하는 아이템 갯수가 확실하지 경우
    - `숫자px`
  - ### `grid-auto-flow`
    - 배치하지 않은 아이템을 어떤 방식의 자동 배치 알고리즘으로 처리할지 정의
    - `row` : 각 행 축을 따라 차례로 배치
    - `row dense` 각 행 축을 따라 차례로 배치, 빈 영역 메움
    - `column` : 각  축을 따라 차례로 배치
    - `column dense` 각 열 축을 따라 차례로 배치, 빈 영역 메움
  - ### `row-gap` `column-gap` `gap`
    - 각 행과 행 사이, 각 열과 열 사이의 간격을 지정
    - `숫자px`
  - ### `grid`
    - `grid-template-xxx` `grid-auto-xxx` 단축 속성
  - ### `align-content`
    - 콘텐츠 수직 정렬
    - `normal, start, center, end, space-around, space-between, space-evenly, stretch`
  - ### `justify-content`
    - 콘텐츠 수평 정렬
    - `normal, start, center, end, space-around, space-between, space-evenly, stretch`
  - ### `place-content`
    - `align-content` `justify-content` 단축 속성
    - `normal, start, center, end, stretch`
  - ### `align-items`
    - 아이템 수직 정렬
    - `normal, start, center, end, stretch`
  - ### `justify-items`
    - 아이템 수평 정렬
    - `normal, start, center, end, stretch`
  - ### `place-items`
    - `align-items` `justify-items` 단축 속성
    - `normal, start, center, end, stretch`
- ## Grid item 속성
  - ### `grid-row-start` `grid-row-end` `grid-column-start` `grid-column-end`
    - 그리드 선의 시작 위치와 끝 위치 지정
    - `숫자, 선 이름, span`
  - ### `grid-row` `grid-column`
    - 각각 `grid-row-xxx` `grid-column-xxx` 단축 속성
  - ### `grid-area`
    - `grid-row` `grid-column` 단축 속성
  - ### `align-self`
    - 단일 그리드 아이템 수직 정렬
    - `normal, start, center, end, stretch`
  - ### `justify-self`
    - 단일 그리드 아이템 수평 정렬
    - `normal, start, center, end, stretch`
  - ### `place-self`
  - `align-self` `justify-self` 단축 속성
  - ### `order`
    - 그리드 아이템이 자동 배치되는 순서 변경
    - 숫자가 작을수록 앞에 배치
  - ### `z-index`
    - 아이템이 쌓이는 순서 변경
