parseFloat
==========
    문자열의 앞부분에서 실수 부분을 추출
    뒷부분의 실수 추출 불가
```js
var height = "135.5입니다";
> parseFloat(height);
< 135.5

var height2 = "내 키는 135.5입니다";
> parseFloat(height2);
< NaN
```