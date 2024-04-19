## `@charset`
- 스타일 시트에 쓰이는 문자 인코딩 지정
- `@charset "utf-8";`

## `@color-profile`
- `color()` 함수에서 색상을 지정하는데 사용할 수 있는 색상 프로필을 정의하고 이름 지정
- ```
  @color-profile --swop5c {
    src: url("https://example.org/SWOP2006_Coated5v2.icc");
  }
  ```

## `@container`
- 컨테이너 쿼리
- 미디어 쿼리와 같이 문서의 **반응형**으로 지정
- 미디어 쿼리는 **디바이스 또는 미디어 유형 기반으로 뷰포트**에 의해 반응
- 컨테이너 쿼리는 **페이지 내의 특정 컴포넌트 요소 기반**으로 반응
- 미디어 쿼리의 상위호환
- 특정 요소 크기에 따라 반응적 동작
### 사용법
#### 1. 반응형으로 등록할 요소를 컨테이너로 등록
  - `container-name`을 통해 쿼리 컨테이너 이름 지정
  - ```
    태그명 {
      container-name: div-container; /* 컨테이너 쿼리 요소 이름 */
    }
    ```
#### 2. 컨테이너 요소의 타입 지정
  - `container-type`에는 `size`, `inline-size`, `normal` 속성값 존재
    + `inline-size` : 인라인 레벨 기준, 요소의 `width` 값에 따라 반응형 동작
    + `size` : 블록 레벨 기준, 요소의 `width` `height` 값에 따라 반응형 동작
    + `normal` : 해당 값이 부여된 요소를 container에서 제외 일종의 none 의미
  ```
  태그명 {
      container-name: div-container;
      container-type: inline-size; /* 왠만한 상황에선 inline-size 로 이용한다고 보면 된다 */
  }
  ```
  ```
  태그명 {
      /* container-name / container-type */
      container : div-container / inline-size; /* 한줄로도 단축 표현이 가능하다 */
  }
  ```
#### 3. @container 반응 치수 지정
  - @conatiner 쿼리를 등록, 컨테이너 이름을 지정해주면 특정 컨테이너 내에서만 반응, 지정 안하면 모든 컨테이너에 대해 전역으로 반응
  ```
  /* 모든 컨테이너 요소에 반응 */
  @container (min-width: 700px) {
    태그명 {
      font-size: 2em;
    }
  }
  
  /* 특정 container-name의 요소에 반응 */
  @container div-container (min-width: 700px) {
    태그명 {
      font-size: 2em;
    }
  }
  ```
### 컨테이너 쿼리 길이 단위
- cqw : 컨테이너 쿼리 너비 1%
- cqh : 컨테이너 쿼리 높이 1%
- cqi : 컨테이너 쿼리 인라인 크기 1%
- cqb : 컨테이너 쿼리 블록 크기 1%
- cqmin : cqi 또는 cqb 중 더 작은 값
- cqmax : cqi 또는 cqb 중 더 큰 

## `@counter-style`
- 카운텅 넘버 스타일 정의
- `<ul> <ol> 등` 카운팅 스타일에 이용
```
@counter-style thumbs {
  system: cyclic;
  symbols: "\1F44D";
  suffix: " ";
}

ul {
  list-style: thumbs;
}
```

## `@font-face`
- 사용자 정의 글꼴 지
## `@font-feature-values`
## `@font-palette-values`
## `@import`
## `@keyframes`
## `@layer`
## `@media`
## `@namespace`
## `@page`
## `@property`
## `@scope`
## `@starting`
## `@supports`
