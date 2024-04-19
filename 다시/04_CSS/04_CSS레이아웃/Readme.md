# Flex Box
- `display`에 `flex`를 설정하면 코드의 자식 요소가 가로 정렬로 바뀜
- 수평된 주축을 기점으로 시작점에서 끝점 방향으로 자식 요소들이 정렬

![Flex Layout](https://velog.velcdn.com/images/front-ant/post/b98ba153-3c96-4c15-98b6-0ab1c9c63f5d/image.png)

- flex 설정 코드는 `flex container` 설정 코드 자식 요소는 `flex items`라고 불림
- `display:inline-flex` 는 `flex container` , `flex items` 모두 인라인
- `display:flex` 는 `flex container`는 블록, `flex items` 는 인라인
  - ## `flex container`
    - ### `flex-flow`
      + flex-direction + flex-wrap 약식 속성
    - ### `flex-direction`
      + 주 축 설정
      + `row, row-reverse, column, column-reverse`
    - ### `flex-wrap`
      + flex items의 줄바꿈 여부 결정
      + `nowrap, wrap, wrap-reverse`
    - ### `justify-content`
      + 주 축 정렬 방법
      + `flex-start, flex-end, center, space-between, space-around, space-evenly`
    - ### `align-content`
      + 교차 축(수직)의 **여러 줄** 정렬 방법
      + `stretch, flex-start, flex-end, center, space-between, space-around`
    - ### `align-items`
      + 교차 축(수직) **한 줄** 정렬 방법
      + `stretch, flex-start, flex-end, center, space-between, space-around`
  - ## `flex items`
    - ### `order`
      + flex items 정렬 순서 정해줌
      + `0, 숫자(음수 가능)`
    - ### `flex-grow`
      + flex items의 증가 너비 비율 설정
      + `0, 숫자`
    - ### `flex-shrink`
      + flex items의 감소 너비 비율 설정
      + `0, 숫자`
    - ### `flex-basis`
      + flex items의 공간 배분 전 기본 너비
      + `auto, 단위(px, em, rem 등)`
    - ### `align-self`
      + 교차 축의 특정 요소 위치만 지정
      + `auto, stretch, flex-start, flex-end, center, space-between, space-around`

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
- ## 속성
  - ### `display`
    - 컨테이너 정의
    - `grid, inline-grid`
  - ### `grid-template-rows` `grid-template-columns` `grid-template`
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
  - ### `grid-auto-rows` `grid-auto-columns` `grid-auto-flow`
  - ### `row-gap` `column-gap` `gap`
  - ### `grid`
  - ### `align-content` `justify-content` `place-content`
  - ### `align-items` `justify-items` `place-items`

# Media Query

