메서드
======
> 함수가 객체의 속성 값이 될 경우 메서드(method)라고 부른다
```js
function f() {
    console.log("f is called");
}

var o = {name:"object", method:f};

f();
o.method();

< f is called
< f is called
```

