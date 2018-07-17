변수
==================
**프로그램 실행 도중 임의 값을 저장해 두고 읽을 수 있는 공간**
### 변수의 선언과 초기화
+ 선언    
    컴퓨터에게 변수를 사용할 것이라고 선언 역할
    ```js
    var variable_name;
    variable_name = value;
    ```
+ 초기화   
    선언한 변수에 처음으로 값을 저장하는 과정 
+ 변수에 값을 저장하는 법 
    - 대입연산자(=)를 활용
    - 콤마(,)를 활용해 여러 변수를 동시에 선언, 초기화 가능
#### 변수의 활용
변수의 이름을 사용하면 변수의 값을 읽어서 사용 가능
```js
var var1 = "1", var2 = "2", var3 = "3";

console.log(var1);
alert(var2);
prompt(var3);
```
### Scope(스코프)
**선언한 변수가 유효한 영역**
#### function scope
+ 선언된 변수는 선언된 함수 안에서 접근 가능
+ 선언된 함수 안에서 선언된 함수 (nested function)에서도 접근 가능
```js
function a() {
    var v_a = "a";
    
    function b() {
        var v_b = "b";
        console.log("b:", typeof (v), typeof (v_a), typeof (v_b));
    }
    
    b();
    
    console.log("a:", typeof (v), typeof (v_a), typeof (v_b));
}

var v = "v";

a();

console.log("o:", typeof (v), typeof (v_a), typeof (v_b));

< b:string string string
< a:string string undefined
< o:string undefined undefined 
```
> block scope(블록의 유효 범위)
초기의 자바스크립트는 변수의 유효 범위가 함수의 유효 범위(function scope)였지만,  
현재의 자바스크립트에서는 변수의 유효 범위가 블록의 유효 범위(block scope)를 따를 수도 있다.  
변수는 자신이 선언된 블록 안에서만 접근 할수 있다.  
변수를 블록의 유효 범위를 따르도록 선언하려면 var 대신 let을 사용한다.
```js
function test() {
    for (let i=0; i>3; i++) {
        console.log("typeof(i) inside the block:", typeof (i));
    } 
    console.log("typeof(i) outside the block:", typeof (i));
}
```
### shadowing (셰도잉)
+ 함수 바깥에서 선언한 변수와 이름이 같은 변수를 함수 안에서도 사용하는 경우 , 함수 바깥에 있는 변수는 잠시 가려진다.(변수 가림 현상을 셰도잉 효과라고 한다)
+ 함수 안에서는 해당 함수에서 선언한 변수를 사용할 수 있다.(함수 바깥에 있는 가려진 변수의 값은 변하지 않는다)
+ 함수에서 빠져나오면 다시 해당 영역에서 선언한 변수(함수 바깥에 있는 변수)에 접근할 수 있다
+ 함수 안에서만 값이 유지되어야 하는 변수는 그 함수 안에서 var 키워드로 선언하고 사용한다
```js
function shadowing_example() {
    var val = 5;
    console.log("F", val);
    val++;
}

var val = 0;
shadowing_example();
console.log("o", val);

< F 5
< o 0
```