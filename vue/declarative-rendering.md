선언적 랜더링
=============
간단한 템플릿 구문을 사용해 선언적으로 DOM에 데이터를 동적 랜더링
```html
<div id="app">
    {{ message }}
</div>

<script src="https://unpkg.com/vue"></script>
<script>
var app = new Vue ({
    el: '#app',
    data: {
        message: '안녕하세요 Vue!'
    }
})
</script>
```