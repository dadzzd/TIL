JSON(JavaScript Object Notification)
====================================
> **`자바스크립트의 객체를 문자열로 표현하는 방법`**  
> 프로그램간에 전달하기 편리 (서버 -> 브라우저)
### JSON API
+ JSON.stringify(object)
    - 인자로 받은 객체를 JSON 문자열로 반환
+ JSON.parse(string)
    - 인자로 받은 문자열을 JavaScript Object로 변경해 반환
```js
var original_obj = {pi:3.14, str:"string"};

var json_str = JSON.stringify(original_obj);
// 반환 문자열 : {"pi":3.14, "str":"string" }

var parsed_obj = JSON.parse(json_str);

console.log(original_obj); // {pi: 3.14, str: "string"}
console.log(parsed_obj); // {pi: 3.14, str: "string"}
```
> **undefined, function 은 변환되지 않는다!**
### AJAX + JSON
+ AJAX를 통해 JSON 데이터를 받는다
```js
var req = new XMLHttpRequest();

req.onreadystatechange = function() {
  if (this.readyState == 4) {
      ...
  } 
}

req.open("GET", JSON_DATA_URL);
req.send();
```
+ `JSON.parse` API를 이용해 받아온 JSON 문자열 데이터를 JavaScript 객체로 변환
```js
req.onreadystatechange() = function() {
    if (this.readyState == 4) {
        data = JSON.parse(this.response);
        ...
    } 
}
```
+ 데이터를 처리하는 JavaScript 프로그램 실행 (HTML 문서에 반영)
    - 데이터가 여러개인 경우 (배열 형태로 값을 받은 경우) 반복문으로 각각의 데이터에 대해 처리
```js
for (var i=0; i<data.length; i++) {
    document.write(data[i].id, data[i].msg);
} 
```