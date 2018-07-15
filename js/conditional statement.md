조건문
======
### if
```js
if (조건식) {
    참인 경우 실행 코드
}

if (true) {
    항상 조건식 성립, 코드 실행
}

if (false) {
    항상 조건식이 거짓, 코드 미 실행
} 
```
### else if
```js
else if (조건식) {
    if 문의 조건이 거짓이고, 위의 조건식이 참일 경우 코드 실행
}
```
+ 중괄호 생략 가능
    ```js
    if (true) {
    console.log("1")''
  }
  else {
    console.log("2");  
    }
  
  if (true) console.log("1");
    else console.log("2");
    ```
### else
```js
else {
    모든 if, else if 문이 모두 실행되지 않았을때 코드 실행
}
```
> 조건식 안에 숫자나 문자열이 있어도 if 조건문이 동작.  
이 경우에는 숫자가 0 일때와 문자열이 빈 문자열 일떄만 거짓으로 인식  
입력할 때 실수하기 쉽고 코드 가독성이 어려워지므로 비사용 권장