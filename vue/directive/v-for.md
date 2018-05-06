v-for
=====
```html
<div id="app">
    <ol>
        <li v-for="todo in todos">
            {{ todo.text }}
        </li>
    </ol>
</div>
<script src="https://unpkg.com/vue"></script>
<script>
    var app = new Vue({
        el: '#app',
        data: {
            todos: [
                { text: 'JavaScript' },
                { text: 'Vue' },
                { text: 'Something' }
            ]
        }
    })
</script>
```