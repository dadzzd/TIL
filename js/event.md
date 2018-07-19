이벤트
======
### Callback Function
> 조건을 등록하고 그 조건이 만족했을 때, 호출되는 함수
#### setTimeout(function, time)
+ time 시간이 지난경우 function 함수를 콜백하는 함수
+ millisecond(1/1000초) 단위
+ timerId를 반환
#### clearTImeout(timerId)
+ setTImeout 함수 호출의 결과로 반환된 timerId를 인자로 받아 예약되어 있던 function 호출을 취소
    - 이미 function이 호출된 경우(시간이 지나 이벤트가 발생한 경우)에는 효과 없음
#### setInterval(function, time)
+ time 시간이 경과할 때마다 function 함수를 콜백하는 함수
+ timerId를 반환함
#### clearInterval(intervalId)
+ setInterval 함수 호출의 결과로 반환된 intervalId를 인자로 받아 주기적으로 호출되던 function 호출을 취소
### 브라우저에서 발생하는 Event 종류
+ form event : HTML 문서의 form element에 변화가 생기거나 submit 버튼 등이 눌렸을 때 발생하는 이벤트
+ window event : 페이지가 모두 로드되었을때 발생하는 이벤트로 onload event가 대표적이다
+ mouse event : 사용자가 마우스를 조작했을 때 발생하는 이벤트
+ key event : 사용자가 키보드를 조작했을 때 발생하는 이벤트
    > ### **이벤트와 이벤트 핸들러**
    > 브라우저에서 다양한 이유(사용자 조작이나 장치 환경의 변화 등)로 발생하는 사건을 이벤트(event)라고 한다.  
    그리고 이러한 이벤트에 대처하는 프로그램을 이벤트 핸들러(event handler)라고 한다. 주로 함수 하나로 구성된다.
    > 이벤트가 발생하고 해당 핸들러(handler)가 호출되는 과정을 이벤트가 '파이어(fire)한다' 거나 '트리거(trigger) 된다'고 표현한다.
### Event
+ click : mouse event로 HTML element를 마우스로 클릭한 경우 발생
+ change : form event로 form 엘리먼트의 내용이 변경된 경우 발생
+ keydown : key event로 key가 눌린 경우 발생
    - EventHAndler에서 return false 시 키 입력 비활성
    - 실제로는 keydown event -> keypress event -> key event 순으로 이벤트가 발생하며, keypress event 발생시에 키가 입력된다.  
    keydown event 에서 return false 를 한경우 keypress event가 이어서 발생하지 않는다
+ submit : form 태그의 submit 이벤트
    - EventHandler에서 return false 시 브라우저 자체 기능(페이지 이동) 비활성
### HTML Tag의 속성에서 EventHandler 설정
+ on **Event** 속성 사용 (onclick, onchange, onkeydown, ...)  
```html
<h1 onclick="console.log('clicked');">..</h1>
<input type="text" onchange="console.log('changed');" onkeydown="console.log('typed');">
```
### JavaScript에서 EventHandler 설정
+ Element의 `"on"+"이벤트"`의 속성에 메소드를 직접 지정
```js
document.getElementById("form1").onsubmit = function eventHandler() {
  console.log("from property");
  return false; // 브라우저의 submit 처리 비활성
};
```
### addEventListner
+ element의 addEventListener(이벤트, 함수) 메소드를 호출해, eventHandler 등록
    - 여러개의 이벤트 핸들러를 등록할 수 있다
```js
document.getElementById("idName").addEventListener(
    "submit",
    function eventHandler() {
        console.log("from addEventListener");
        return false;
    }
);
```
### removeEventListener
+ element의 removerEventListener(이벤트, 함수) 메소드를 호출해, eventHandler 삭제