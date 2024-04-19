# 플렉스
- `display`에 `flex`를 설정하면 코드의 자식 요소가 가로 정렬로 바뀜
- 수평된 주축을 기점으로 시작점에서 끝점 방향으로 자식 요소들이 정렬

![flex](https://velog.velcdn.com/images/front-ant/post/b98ba153-3c96-4c15-98b6-0ab1c9c63f5d/image.png)

- flex 설정 코드는 `flex container` 설정 코드 자식 요소는 `flex items`라고 불림
- `display:inline-flex` 는 `flex container` , `flex items` 모두 인라인
- `display:flex` 는 `flex container`는 블록, `flex items` 는 인라인
  - ## `flex container`
  - `flex-flow` : flex-direction + flex-wrap 약식 속성
  - `flex-direction` : 주 축 설정
    + `row, row-reverse, column, column-reverse`
  - `flex-wrap` : flex items의 줄바꿈 여부 결정
    + `nowrap, wrap`
  - `justify-content` : 주 축 정렬 방법
    + `flex-start, flex-end, center, space-between, space-around`
  - `align-content` : 교차 축(수직)의 **여러 줄** 정렬 방법
    + `stretch, flex-start, flex-end, center, space-between, space-around`
  - `align-items` : 교차 축(수직) **한 줄** 정렬 방법
    + `stretch, flex-start, flex-end, center, space-between, space-around`
  - ## `flex items`
  - `order` : flex items 정렬 순서 정해줌
    + `0, 숫자(음수 가능)`
  - `flex-grow` : flex items의 증가 너비 비율 설정
    + `0, 숫자`
  - `flex-shrink` : flex items의 감소 너비 비율 설정
    + `0, 숫자`
  - `flex-basis` : flex items의 공간 배분 전 기본 너비
    + `auto, 단위(px, em, rem 등)`
  - `align-self` : 교차 축의 특정 요소 위치만 지정
    + `auto, stretch, flex-start, flex-end, center, space-between, space-around`
# 오버플로우

# 불투명도

# z-index
