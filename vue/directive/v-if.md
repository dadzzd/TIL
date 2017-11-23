# v-if
```html
<div id="app">
    <p v-if="seen">이제 나를 볼 수 있어요</p>
</div>
<script src="https://unpkg.com/vue"></script>
<script>
    var app = new Vue({
        el: '#app',
        data: {
            seen: true;
        }
    })
</script>
```