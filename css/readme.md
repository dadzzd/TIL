CSS
====
> Cascading Style Sheet
+ CSS는 HTML 문서의 요소가 어떻게 표시될지 정의
+ CSS를 작성할 때는 [선택자] {[속성 이름]:[값];...} 형태로 사용
+ CSS는 우선순위가 가장 높은 HTML 태그 안에 정의한 스타일을 가장 먼저 반영하고, 다음으로 스타일 태그 안에 적용한 스타일,
다음으로 링크를 통해 외부 파일에서 불러온 스타일을 반영
### 문법
`[selector] { [property_name] : [value]; ... }`
+ selector : tag name, id, class로 작성 가능
    - tag name : tag name 그대로 사용 (h1, h2, p, img, ....)
    - id : #을 붙이고 id 사용 (#name, #id, ...)
    - class : .을 붙이고 class name 사용 (.classname, ...)
+ property_name : selector에 해당하는 엘리먼트의 style 속성
+ value : 앞에 정의한 style property의 값
### 적용하기
1. head 태그 안에서 link 태그를 이용해 외부 파일 불러오기
```html
<link rel="stylesheet" href="[css file]">
```
2. head 태그 안에서 style 태그를 이용해서 정의하기
```html
<style>
    ...
</style>
```
3. 태그 안에 직접 style 속성을 이용해서 정의하기
```html
<p style="color:red">...</p>
```
### CSS 적용 우선 순위
1. html element 안에서 적용한 스타일
2. style tag 안에서 적용한 스타일
3. link를 통해 외부 파일에서 적용한 스타일
### 주석
```css
h2 {
    color: green; /* 글자색은 초록색으로 */
}

```