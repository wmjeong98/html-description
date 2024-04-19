# 플렉스 `flex`
- `display`에 `flex`를 설정하면 코드의 자식 요소가 가로 정렬로 바뀜
- 수평된 주축을 기점으로 시작점에서 끝점 방향으로 자식 요소들이 정렬

![flex](https://velog.velcdn.com/images/front-ant/post/b98ba153-3c96-4c15-98b6-0ab1c9c63f5d/image.png)

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
  
# 오버플로우 `overflow`
- 특정 요소의 자식 요소가 부모 요소의 범위를 초과할 때 어떻게 처리 할지를 결정할 수 있는 속성
- ## `visible`
  - 범위를 넘어 가더라도 그대로 보여줌
- ## `hidden`
  - 범위를 넘어가는 자식요소의 부분은 보이지 않음
- ## `scroll`
  - 범위를 넘어가는 자식요소의 부분은 보이지 않지만 사용자가 확인할 수 있는 스크롤바 표시
- ## `auto`
  - 범위를 넘어가는 자식요소의 부분이 있을 경우 보이지 않도록 하고 사용자가 확인할 수 있는 스크롤바 표시
- ## `overflow-x` `overflow-y`
  - 가로부분 세로부분 각각 적용되는 속성값

# 불투명도 `opacity`
- 대상의 불투명도를 나타냄
- ## 속성값 : 0.0 ~ 1.0, 0% ~ 100%

# z-index
- 자식 또는 하위의 아이템의 Z축 순서를 지정
- 값을 가진 요소가 클수록 작은 요소를 덮음 -> 겹쳐진 여러 요소들의 우선순위를 정함
- ## `auto`
  - 부모 요소와 같은 값
- ## `숫자`
  - 숫자가 높을수록 우선순위 높음
    - 숫자와 auto 모두 같은 값일 경우, 더 마지막에 정의한 요소가 우선순위 높음
- ## `inherit`
  - 상위 요소의 값 상속
- ## `initial`
  - 기본값 사용
- ## `unset`
  - 상속값이 있으면 상속값 적용, 아니면 기본값 사
