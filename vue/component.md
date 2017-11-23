# component
컴포넌트란 그 자체로 제 기능을 하며 크기는 작고, 재사용할 수 있는 컴포넌트로 구성된 대규모 응용 프로그램을 구축할 수 있게 해주는 추상적 개념.
모든 유형의 응용 프로그램 인터페이스를 컴포넌트 트리로 추상화 가능.
```html
<div id="app">
    <ol>
        <todo-item
            v-for="item in groceryList"
            v-bind:todo="item"
            v-bind:key="item.id">
        </todo-item>
    </ol>
</div>
<script src="https://unpkg.com/vue"></script>
<script>
    Vue.component('todo-item', {
        props: ['todo'],
        template: '<li>{{ todo.text }}</li>'
    })
    var app = new Vue({
        el: '#app',
        data: {
            groceryList: [
                { id: 0, text: 'Vegetavles' },
                { id: 1, text: 'Cheese' },
                { id: 2, text: 'Whatever lese humans are supposed to eat' }
            ]
        }
    })
</script>
```
자식을 props 인터페이스를 통하여 부모로부터 합리적인 수준으로 분리할 수 있다.
부모 앱에 영향을 주지 않으면서 <todo-item> 컴포넌트를 더 복잡한 템플릿과 로직으로 향상 시킬 수 있다.
대규모 응용 프로그램에서는 컴포넌트로 전체 앱을 나누는 것이 필수 적이다.
```html
<div id="app">
    <app-nav></app-nav>
    <app-view>
        <app-sidebar></app-sidebar>
        <app-content></app-content>
    </app-view>
</div>
```