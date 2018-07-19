이벤트
======
### Callback Function
> 조건을 등록하고 그 조건이 만족했을 때, 호출되는 함
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