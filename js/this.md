this
=====
> 함수가 호출되었을 때 어떤 객체에 바인드된 속성으로 호출된 것인지를 보여 주는 예약어
```js
function f() {
    console.log(this);
    console.log("f is called");
}

var o = {name:"object", method:f};

f();
o.method();

< window {postMessage: f, blur: f, focus: f, close: f, frames: window, ...}
f is called
< {name: "object", method: f}
f is called
```
```js
function f() {
    console.log(this);
    console.log("f is called");
}

function setName(name) {
    this.name = name;
}

var o = {name:"object", method:f, setName:setName};
var o2 = {name:"", setName:setName};

o.setName("object1");
o2.setName("object2");

console.log(o, o2);
```