# HTML 7장
## iframe
- 웹 페이지 내에 웹 페이지를 표시하는 데 사용
- inline frame = iframe `<iframe>`
- `<iframe src="url" title="description"></iframe>`
- `width="숫자"` `height="숫자"`로 너비와 높이 설정
- 테두리 제거는 `style border` 사용
- 색상 및 크기 변경 가능
- `<iframe>`은 `name` 사용 // `<a>`는 `target`

## 자바스크립트
- `<script>` 태그 사용
- `document.getElementById("아이디이름")` 가장 자주 사용하는 메소드

## 파일 경로
- 웹 사이트의 폴더 구조에서 파일의 위치를 설명
- **절대 파일 경로**
  + 파일의 전체 URL
- **상대 파일 경로**
  + 현재 페이지를 기준으로 하는 파일
- 상대 파일 경로를 사용하는 것이 가장 좋음

## Head 요소
### `<head>` 요소
- `<head>` 요소는 메타데이터에 표시, `<html>` 태그와 `<body>`태그 사이에 배치
- HTML 메타데이터는 HTML 문서에 대한 데이터, 표시는 X
- 메타데이터는 일반적으로 문서 제목, 문자 집합, 스타일, 스크립트 및 기타 메타 정보를 정의
### `<title>` 요소
- 문서의 제목, 텍스트 전용
- 페이지 제목의 내용은 검색 엔진 최적화에 매우 중요(SEO: Search Engine Optimization, 내 웹사이트를 구글이나 네이버와 같은 검색엔진의 검색결과 상단에 노출시킬 수 있도록 최적화하는 방법)
- SEO는 비용을 들이지 않고 기존에 가지고 있는 콘텐츠만을 활용하여 무료 트래픽을 확보할 수 있게 해준다는 점
### `<style>` 요소
- 스타일 정보 정의
### `<link>` 요소
- 현재 문서와 외부 리소스 간의 관계
- 외부 스타일시트에 연결하는데 가장 자주 사용
### `<meta>` 요소
- charset, 페이지 설명, 키워드, 문서 작성자, 뷰포트 설정에 사용
- 페이지에 표시 X, 검색 엔진(키워드) 및 기타 웹 서비스에 의해 브라우저에서 사용됨
- `name content charset http-equiv`
- 뷰포트 설정
  + 웹 페이지에서 사용자가 볼 수 있는 영역
  + 장치에 따라 다름
  + ```
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    ```
### `<script>` 요소
- 자바스크립트 정의
  ```
  <script>
  function myFunction() {
    document.getElementById("demo").innerHTML = "Hello JavaScript!";
  }
  </script>
  ```
### `<base>` 요소
- 페이지의 모든 relative URL에 대한 기본 URL과 타겟을 지정

## 레이아웃
![레이아웃 요소](https://www.w3schools.com/html/img_sem_elements.gif "레이아웃 요소")
- `<header>` : 문서 또는 섹션의 머리글을 정의
- `<nav>` : 메뉴 요소
- `<section>` : 제목별로 나눌 수 있는 요소
- `<article>` : 개별 콘텐츠를 나타내는 요소
- `<aside>` : 좌우측 사이드바를 나타내는 요소
- `<footer>` : 제작자의 정보나 저작권의 정보를 나타내는 요소
- 레이아웃 기법
  + CSS 프레임워크
  + CSS float 레이아웃
  + CSS flex-box 레이아웃
  + CSS grid 레이아웃

## 반응형 웹 디자인
- 모든 장치에서 잘 보이는 웹 페이지를 만드는 것
- 다양한 화면 크기와 뷰포트에 맞게 자동으로 조정
- 자동으로 크기 조정, 숨기기, 축소/확대하는 것
- 뷰포트 설정 : `<meta name="viewport" content="width=device-width, initial-scale=1.0">`
- 반응형 이미지 : CSS에서 `max-width:100%;height:auto` 로 설정
- 브라우저 너비에 따른 이미지 표시 :
  ```
  <picture>
    <source srcset="img_smallflower.jpg" media="(max-width: 600px)">
    <source srcset="img_flowers.jpg" media="(max-width: 1500px)">
    <source srcset="flowers.jpg">
    <img src="img_smallflower.jpg" alt="Flowers">
  </picture>
  ```
- 반응형 텍스트 크기 : 뷰포트 너비를 의미하는 `vw` 단위로 설정 `<h1 style="font-size:10vw">Hello World</h1>`
- 뷰포트는 브라우저 창 크기, 1vw = 뷰포트 너비의 1%. 뷰포트 너비가 50cm인 경우 1vw는 0.5cm
- 미디어 쿼리 : 브라우저 크기마다 완전히 다른 스타일을 정의 가능
  ```
  <style>
  .left, .right {
    float: left;
    width: 20%; /* The width is 20%, by default */
  }
  
  .main {
    float: left;
    width: 60%; /* The width is 60%, by default */
  }
  
  /* Use a media query to add a breakpoint at 800px: */
  @media screen and (max-width: 800px) {
    .left, .main, .right {
      width: 100%; /* The width is 100%, when the viewport is 800px or smaller */
    }
  }
  </style>
  ```
