# 태그
## 태그의 속성
- 태그의 속성은 <태그 속성 = "값"> 의 형태로 사용하며, 태그마다 여러 속성을 부여할 수 있음
- HTML에서 태그의 속성 또한 미리 정의되어 있으며, 태그 속성에 맞는 값을 입력하면 특별한 기능을 하게됨
```html
<html>
<head>
	<link type="text/css" href="my_style.css">
</head>
<body>
	<font color="red" face="Dotum">Hello</font>
	<font color="yellow">World</font>
</body>
</html>
```
## id, class 속성
- 모든 태그에는 id 속성과 class 속성을 지정해 줄 수 있는데, 이를 이용하면 `CSS`나 `JavaScript`에서 태그를 좀더 쉽게 다룰 수 있음
- id는 원칙상 **하나의 id** 당 **하나의 태그**에만 적용할 수 있으며, class는 **하나의 class**를 **여러 태그**에 적용할 수 있음
```
<div id="my-box1"></div>
<div id="my-box2" class="boxes"></div>
<div id="my-box3" class="boxes"></div>
<div class="boxes"></div>
```
- <a> 태그 id 속성에 이름을 넣고 href 속성에 **"# + 이름"** 으로 조합하여 넣고 클릭하면 id 속성에 해당 이름이 있는 곳으로 이동
```
<a id="이동위치이름">이동할 위치</a><a href="#이동위치이름"> 위치 이동 클릭</a>
```
- id 속성을 지정하지 않아도 브라우저 상단 끝으로 이동할 수 있는 **#top**이 있지만 **하단 이동은 id 속성을 이용해야 한다.**
## style 속성
- 태그의 스타일, 즉 보이는 형태를 정의하는 속성
- HTML 자체의 기능이라기 보다는 **CSS의 속성**을 HTML 문서 내에서 태그에 직접 설정할 때 쓰이는 속
```
<div style="width:500px; height:300px"></div>
<div style="height:40px; border: 1px solid green">mybox</div>
```
