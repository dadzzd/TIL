클로저
======
```js
function makeCounterFunction(initVal) {
    var count = initVal;
    function Increase() {
        count++;
        console.log(count);
    }
    return Increase;
}

var counter1 = makeCounterFunction(0);
var counter2 = makeCounterFunction(10);

counter1();
counter2();

< 1
< 11
```
> 클로저는 자바스크립트의 함수와 그 함수가 선언될 떄의 환경(environment)으로 이뤄진다

makeCounterFunction(0) | makeCounterFunction(10)
-----------------------|-------------------------
클로저가 가리키는 함수 | function Increase(){} | function Increase(){}
클로저의 환경 | var count = 0; | var count = 10;
> 클로저를 이용하면 다른 객체 지향 언어에 있는 private, public 같은 개념을 구현 할 수 있다