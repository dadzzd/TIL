# v-on
```html
<div id="app">
    <p>{{ message }}</p>
    <button v-on:click="reverseMessage">메시지 뒤집기</button>
</div>
<script src="https://unpkg.com/vue"></script>
<script>
    var app = new Vue({
        el: '#app',
        data: {
            message: '안녕하세요! Vue.js!'
        },
        methods: {
            reverseMessage: function() {
                this.message = this.message.split('').reverse().join('')
            }
        }
    })
</script>
```