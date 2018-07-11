parseInt
========
문자열의 앞부분에서 정수 부분을 추출하는 명령어
------------------------------------
    뒷부분의 정수 추출 불가
```js
var height = "123입니다";
> parseInt(height);
< 123

var height2 = "내 키는 123입니다";
> parseInt(height2);
< NaN
```