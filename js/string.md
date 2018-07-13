String
======
### 문자열 길이
문자열의 `.length` 속성을 이용 `str.length`
```js
var str = "Hello";
> str.length;
< 5

> str["length"];
< 5

> "hello".length;
< 5
```
### 문자열 붙이기
1. `.concat` 함수 사용
    + `str1.concat(str2)`
        ```js
        var str = "Hello";
        var str2 = "World";
        > str.concat(str2);
        < "HelloWorld"
  
        var str3 = str.concat(str2);
        > str3;
        < "HelloWorld"
  
        > str.concat(str2).concat("!");
        < "HelloWorld!"
  
        > "Hello".concat("World").concat("!");
        < "HelloWorld!"
        ```
2. 더하기(`+`) 연산자 사용
    + `str1 + str2`
        ```js
        > str + str2;
        < "HelloWorld"
  
        > "Hello" + "World";
        < "HelloWorld"
  
        > "Pi is " + 3.14;
        < "Pi is 3.14"
  
        > 3.14 + " is Pi";
        < "3.14 is Pi"
        ```
### 특정위치의 문자열
> 문자열의 인덱스는 0부터
1. `.charAt` 함수 사용
    + 첫 문자 : `str.charAt(0)`
    + 마지막 문자 : `str.charAt(str.length-1)`
    ```js
    var str = "abcdeabcde";
    > str.charAt(0);
    < "a"
 
    > str.length;
    < 10
 
    > str.charAt(9);
    < "e"
 
    > str.charAt(10);
    < ""
 
    > str.charAt(-1);
    < ""
    ```
2. 대괄호([]) 사용
    + 첫 문자 : `str[0]`
    + 마지막 문자 : `str[str.length-1]`
    ```js
    > str[1];
    < "b"
 
    > str[10];
    > undefined
 
    > str[-1];
    < undefined
    ```
    + 뒤에서 n번째 문자열
    ```js
    > str.charAt(str.length - 5);
    < "a"
    ```
### 부분문자열
문자열의 연속된 일부분을 구하는 함수
1. `substring(pos1, pos2)` `pos1`에서 `pos2` 바로 앞 문자열 까지 반환
    ```js
    > str.substring(2, 4);
    < "cd"
    ```
    + `pos2` 생략 시 `pos1` 에서부터 마지막 까지의 문자열 반환
        ```js
        > str.substring(2);
        < "cdeabcde"
        ```     
2. `substr(pos, length)` `pos`에서`length`길이 만큼의 부분 문자열 반환
    ```js
    > str.substr(2,4);
    < "cdea"
    ```
    + `length` 생략시, `pos`에서 마지막까지의 문자열 반환
        ```js
        > str.substr(2);
        < "cdeabcde"
        ```
    + `pos`가 음수인 경우, `str.length - pos`로 동작
        ```js
        > str.substr(-7);
        < "deabcde"
  
        > str.substr(-7, 2)
        < "de"
        ```
### 문자열 검색
1. `indexOf(str)` 문자열이 처음으로 나오는 위치
    ```js
    > str.indexOf("bc");
    < 1
 
    > str.indexOf("f");
    < -1
    ```
2. `lastIndexOf(str)` 문자열이 마지막으로 나오는 위치
    ```js
    > str.lastIndexOf("bc");
    < 6
 
    > str.lastIndexOf("f");
    > -1
    ```