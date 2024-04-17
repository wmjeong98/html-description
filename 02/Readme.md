# HTML 3장
## HTML 텍스트 서식 요소
- `<b>` 굵은 글씨 = 굵음
- `<strong>` 중요 텍스트 = 굵음
- `<i>` 이탤릭체 텍스트 = 기울임
- `<em>` 강조된 표시 = 기울임
- `<mark>` 표시된 텍스트 = 형광펜
- `<small>` 작은 텍스트 = 사이즈 작음
- `<del>` 삭제된 텍스트 = 글자에 줄 그어서 지운 것처럼 표시
- `<ins>` 삽입된 텍스트 = 밑줄
- `<sub>` 아래 첨자 텍스트 = 인덱스
- `<sup>` 위 첨자 텍스트 = 지수

## HTML 인용 및 인용 요소
### `<blckquote>`
- 다른 출처에서 인용하여 섹션을 정의
```
<p>Here is a quote from WWF's website:</p>
<blockquote cite="http://www.worldwildlife.org/who/index.html">
For 60 years, WWF has worked to help people and nature thrive. As the world's leading conservation organization, WWF works in nearly 100 countries. At every level, we collaborate with people around the world to develop and deliver innovative solutions that protect communities, wildlife, and the places in which they live.
</blockquote>
```

### `<q>`
- 따옴표 역할
```
<p>WWF's goal is to: <q>Build a future where people live in harmony with nature.</q></p>
```

### `<abbr>`
- 약어 역할, 점선 밑줄로 표시
- title 속성을 이용하여 사용 커서를 갖다 대면 설명 표시
```
<p>The <abbr title="World Health Organization">WHO</abbr> was founded in 1948.</p>
```

### `<address>`
- 문서 작성자/소유자에 대한 연락처 정보를 정의
- 연락처 정보는 이메일 주소, URL, 실제 주소, 전화 등
- 요소 텍스트는 일반적으로 기울임꼴로 렌더링되며 브라우저는 항상 요소 앞뒤에 줄 바꿈 추가
```
<address>
Written by John Doe.<br>
Visit us at:<br>
Example.com<br>
Box 564, Disneyland<br>
USA
</address>
```

### `<cite>`
- 창작물 표시 역할
- 사람의 이름은 안됨
- 기울임꼴로 렌더링
```
<p><cite>The Scream</cite> by Edvard Munch. Painted in 1893.</p>
```

### `<bdo>`
- Bi-Directional Override의 약자
- 텍스트 방향을 거꾸로 사용하는데 이용
```
<bdo dir="rtl">This text will be written from right to left</bdo>
```

## 주석
`<!-- contents -->`
