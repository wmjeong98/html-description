# `<head>`
- 기계가 식별할 수 있는 문서 정보를 담는 역할
# `<title>`
- 문서 제목 요소
- SEO 큰 영향 , 상세한 제목이 더 좋은 성과가 나타남
# `<base>`
- 모든 상대 URL이 사용할 기준 URL
- `href` : 기준 URL
- `target` : 결과를 보여줄 표시
# `<link>`
- 현재 문서와 외부 리소스의 관계 명시
- 스타일 연결을 제일 많이 쓰지만, 사이트 아이콘 연결 등으로도 쓰임
- `href` : 연결시킬 URL
- `rel` : 연결시킬 URL와의 관계 명시
- `media` : 미디어 유형이나 쿼리 지정
# `<style>`
- 문서나 문서 일부에 대한 스타일 정보 포함
- `media` : 스타일을 적용할 매체, 미디어 쿼리, 기본값 all  
# `<meta>`
- 메타관련 요소 -> 메타데이터
- `charset` : 페이지 문자 인코딩
- `content` : `http-equiv`, `name` 값 담음
- `http-equiv` : HTTP 헤더에 정보 또는 값을 제공하는 `content` 속성, HTML 문서에서 사용할 문서 종류나 페이지 이동, 새로고침
- `name` : 메타데이터 이름
# `<script>`
- 스크립트 요소
- `src` : 외부 스크립트를 가리키는 URL
- `type` : 스크립트 유형
# `<noscript>`
- 페이지 스크립트 유형을 지원하지 않거나 브라우저가 스크립트를 비활성화한 경우 보여줄 HTML 구획
# `<template>` 
- 콘텐츠 템플릿 요소
- `table` 등으로 템플릿을 만들어놓으면 자바스크립트를 이용하여 그 템플릿에 콘텐츠값을 넣어줌 테이블 한정 DB에 값 넣는거랑 비슷
