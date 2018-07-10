자료형
======
    변수에 저장할 수 있는 값의 종류
#### 자료형의 종류
##### Number
    숫자를 나타내는 자료형
    64bit로 실수와 정수 모두 표현 가능
    정상적이지 않는 숫자나 표현할 수 없는 범위의 수를 표시하는 NaN, Infinity
    "1"은 문자열이고 1은 숫자형
```js
var a = 100, b = 3.14, c = 1e-3;
```
##### String
    작은 따옴표나('), 큰따옴표(")로 감싸서 문자열을 표현
    문자열 안에 따옴표, 큰따옴표 등의 문자를 활용 하려면 이스케이프 문자 활용
    이스케이프 문자 역슬래시(\) 사용
    줄바꿈 \n
    작은 따옴표 \'
    큰따옴표 \"
    역슬래시 \\
```js
var a = 'abcde';
var b = "abcde";
var c = "abc'de";
var d = 'abc"de';
var e = "ab\'c\"de";
var f = 'ab\'c\"de';
var g = "\\abcde";
var h = "abc\nde";
var i = a+b;
```
##### Boolean
    참 거짓
```js
var e = true, f = false;
```