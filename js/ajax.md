AJAX
====
    브라우저에서 페이지를 이동하지 않고 자바스크립트를 통해 HTTP Request를 보내고 받아 JS에서 처리할 수
    사용자에게 더 나은 사용 경험 제공, 대부분의 웹사이트에서 사용되고 있는 기술

####1. AJAX를 위한 객체 생성
```js
var req = new  XMLHttpRequest(); // HTTP 요청을 만들 수 있는 새로운 객체를 생성하는 명령
```
####2. 요청의 방식과 URL 설정
```js
req.open("GET", "./data.txt"); // http request method와 URL 설정
```
####3. 요청 전송
```js
req.send();
```
####4. 응답 확인
    req.response에 저장됨
    비동기 방식으로 요청하기 때문에 send 메소드 호출 후, 바로 코드에서 접근하면 데이터가 비어 있음
    AJAX의 진행에 따라 호출되는 callback 함수를 활용해야 함
#### 브라우저 옵션
###### --disable-web-security 옵션
    브라우저의 보안 정책을 우회하기 위해 사용하는 옵션
    same-origin-policy 비활성화 함
##### readyState 속성
    AJAX 요청에 따라 0~4까지 변화함

 readyState | 의미 |
---------|----------
 0 | open 메소드 호출 전 |
 1 | open 메소드 호출 후, send 메소드 호출 전 |
 2 | 보낸 요청에 대해 응답 헤더가 수신된 후 |
 3 | 응담의 바디 부분이 수신중일 때 |
 4 | 모든 응답이 수신되었을 때
##### onreadystatechange 속성
    readyState가 변할 때마다 호출되는 콜백 함수
##### status 속성
HTTP response의 응답 헤더에 기록된 코드

  Response Code | 의미 |
 ---------------|------|
 200 | OK |
 404 | Not Fount |
 500 | Internal Error |
 ... | ...
##### 응답을 정상적으로 수신한 경우
    readyState : 4
    status: 200
##### 기타 callback function 활용 가능한 속성
    onloadstart
    onprogress
    onabort
    onerror
    onload
    ontimeout
    onloadend
