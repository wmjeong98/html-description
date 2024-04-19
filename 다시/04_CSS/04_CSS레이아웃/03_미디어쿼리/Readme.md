# Media Query
- CSS에서 어떤 스타일을 선택적으로 적용하고 싶을 때 사용
- `@media` 키워드로 시작
- ```
  @media (조건) {
    스타일
  }
  ```
- 스타일 부분에는 일반적인 CSS 코드, 조건 부분이 만족될 때는 스타일 적용, 아닐때는 스타일 무시

## 미디어 쿼리 CSS 적용법
1. HTML `link` 태그의 `media` 속성 값 설정
```
<link href="css/common.css" rel="stylesheet" type="text/css" 
   media="screen and (min-width:0px) and (max-width:480px)">
```  
2. css 파일 내에 직접 `media` 설정
```@media all and (min-width:480px) { ... }```
3. 미디어 쿼리를 설정한 파일을 css 파일 내에서 `import` 해서 적용
```@import "../media.css";```

## 미디어 쿼리 타입 
1. all : 기본값, 모든 장치
2. print : 인쇄 장치
3. screen : 컴퓨터 화면 장치 또는 스마트 기기의 화면
4. speech : 음성 출력 장치, 페이지 읽어주는 화면 낭독기
5. tv : 영상 음성이 동시에 출력되는 장치
6. projection : 프로젝터 장치
7. handheld : 손에 들고 다니는 소형장치
8. aural : 음성 합성 장치
9. embossed : 점자 인쇄 장치
10. tty : 디스플레이 기능이 제한된 장치
11. braille : 점자 표시 장치

## 미디어 쿼리 연산자
- and : 여러 미디어 특징들을 하나로 결합
- , (or) : 쉼표로 분리된 각 목록은 각각 개별 미디어 쿼리
- not : 전체 미디어 쿼리를 부정하기 위해 사용
- only : 미디어 쿼리를 지원하지 않는 브라우저가 주어진 스타일을 적용하는 것을 방지, 미디어 쿼리 결과에 아무런 영향을 미치지 않음
- not 이나 only를 사용하려면 미디어 타입을 규정해야 함

## 미디어 쿼리 속성
- ### min, max 사용 가능 속성
  - #### `width` `height`
    - 뷰 영역의 최소/최대 넓이/높이, 지정 사이즈보다 넓/높 or 좁/낮으면 적용
  - #### `device-width` `device-height`
    - 디바이스 사이즈의 최소/최대 넓이/높이, 지정 사이즈보다 넓/높 or 좁/낮으면 적용
  - #### `aspect-ratio`
    - 뷰포트 너비와 높이의 비율
    - **너비/높이 순**으로 작성
  - #### `device-aspect-ratio`
    - 스크린 너비와 높이의 비율
    - **너비/높이 순**으로 작성
  - #### `color`
    - 출력 장치 색상에 대한 **비트** 수
    - 출력 장치 컬러가 아닌 경우 0의 값에 대응
  - #### `color-index`
    - 기기의 색상 수 
  - #### `monochrome`
    - 출력 장치가 **흑백**인 경우 **픽셀당 비트 수**
    - 출력 장치가 흑백이 아니라면 0의 값에 대응
  - #### `resolution`
    - 출력 장치의 **dpi 해상력**에 대응
    - min, max 접두사는 사각형 아닌 픽셀에도 대응하지만 접두사 없는 `resolution` 조건은 사각형 픽셀에만 대응
    - 조건 값으로는 `dpi` `dpcm` 단위 사용
- ### min, max 사용 X 속성
  - #### `orientation`
    - 세로 길이 혹은 가로 길이 둘 중 하나로 기준 적용
      + portrait : 세로 길이 중심
      + landscape : 가로 길이 중심
  - #### `scan`
    - TV 스캔 방식에 따라 대응
    - progressive 값은 초당 60회 수준의 고화질 스캔에 대응
    - interlace 값은 초당 30회 수준의 일반 스캔에 대응
    - 대부분 HDTV는 progressiv와 interlact 방식 모두 지원
  - #### `grid`
    - 출력 장치가 그리드 방식이면 대응
    - 그리드 방식은 타자기와 같이 고정된 글꼴만 사용하는 장치
    - 통상 출력 장치는 비트맵 아니면 그리드 방식
    - 값은 0과 1뿐이고 0의 값은 비트맵 방식에 대응

## 미디어 쿼리 뷰포트 지정
- 뷰포트 : 모바일 브라우저에서 웹 콘텐츠를 출력하는 영역
- 웹 페이지의 너비와 높이, 확대/축소 설정, 웹 콘텐츠가 최적의 상태로 화면에 표시될 수 있도록 도움
- 지정 방법은 `head` 태그 안에 입력
  ```
  <meta name="viewport" content="width=device-width, maximum-scale=1.0, minimum-scale=1, 
    user-scalable=yes,initial-scale=1.0" />
  ```
- `meta` 태그에서는 px단위 사용하며 단위 표현은 생략
- 복수개의 속성을 사용할 때는 쉼표로 구분
- 일반적으로 모바일 디바이스에만 적용
- ### 뷰포트 속성
  - #### `width` `height`
    - 뷰포트 너비/높이
  - #### `initial-scale`
    - 뷰포트 초기 배율
    - 기본값은 1 (음수 X)
    - 1보다 크면 확대된 페이지, 1보다 작으면 축소된 페이지
  - #### `user-scalable`
    - 뷰포트 확대/축소 여부
    - 속성값은 `yes` `no`
    - 기본값은 `yes`, `no`로 설정하면 사용자가 페이지 확대 X
  - #### `minimum-scale`
    - 뷰포트 최소 축소 비율 지정
    - 기본값은 0.25(음수 X)
  - #### `maximum-scale`
    - 뷰포트 최대 확대 비율 지정
    - 기본값은 5.0(음수 X)
## 다양한 디바이스 해상도

![디바이스 해상도](https://blog.kakaocdn.net/dn/bL535d/btrg1LGWYfL/DUSH1fqtCvvNEphQ2HnxLk/img.jpg)
