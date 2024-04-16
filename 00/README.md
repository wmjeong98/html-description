# HTML
- Hyper Text Markup Language의 약자
- 웹 페이지를 만들기 위한 표준 마크업 언어
- 웹 페이지의 구조를 설명
- 일련의 요소로 구성
- HTML 요소는 브라우저에 콘텐츠를 표시하는 방법을 알려줌
- HTML 요소는 "this is heading", "this is paragraph", "this is link" 등
# 간단한 HTML 문서
```
<!DOCTYPE html>
<html>
<head>
<title>Page Title</title>
</head>
<body>

  <h1>My First Heading</h1>
  <p>My First paragraph.</p>

</body>
</html>
```
# DOCTYPE이란
- **Document Type Definition, DTD**
- 어떤 버전의 HTML을 사용할 것 인지를 인터넷 브라우저에 알려줌 
- HTML은 한 종류가 아니라 여러 종류의 HTML 존재
- **HTML 4.01 Strict, HTML 4.01 Transitional, XHTML 1.0** 등
- 이러한 유형에 따라서 같은 코딩을 하더라도 html 파일 실행 시에 다른 결과 화면으로 나타남
- Doctype 선언할 경우와 하지 않았을 경우, 브라우저에 따라서 다르게 출력
- 최근 많이 사용하는 HTML 5의 경우 **<!DOCTYPE html>** 이라고 선언
- HTML 5의 경우 HTML, XHTML에서 사용되지 않았던 태그들이 많이 추가되어 DOCTYPE을 선언하지 않거나 다른 DOCTYPE을 선언할 경우 새로운 태그들을 사용할 수 없는 경우도 있으므로, 반드시 DOCTYPE 선언해야 함
- HTML 5의 경우 브라우저 **( 익스플로러, 크롬, 오페라, 파이어폭스, 사파리 등 )** 의 버전에 따라서도 사용할 수 있는 태그와 사용이 불가한 태그가 있으므로, **DOCTYPE 선언과 더불어 브라우저 확인도 필요**

# HTML 요소
시작 태그, 일부 콘텐츠 및 끝 태그로 정의
|시작 태그|콘텐츠 요소|끝 태그|
|---|---|---|
|"<h1>"|My Fisrt Heading|/h1|
|p|My Fisrt paragraph|/p|
|br|none|none|


