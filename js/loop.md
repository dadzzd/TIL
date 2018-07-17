반복문
======
### while
+ 조건에 따라 프로그램의 일정 코드를 반복 수행하는 구문
+ 조건을 만족하는 동안에 반복 실행할 코드를 계속 실행
+ continue 키워드를 만나면 뒤에 있는 코드를 모두 건너뛴다
+ break 키워드를 만나면 반복문에서 즉시 탈출### do while
```js
while (조건식) {
    반복 실행 코드
}

var sum = 0;
var i = 0;
while (i<5) {
    sum = sum + i;
    i++;
} 
```
### do while
+ 조건식이 거짓일 때, 한번 실행되고 종료
```js
do {
    반복 실행될 코드
} while (조건식);

do {
    sum = sum + i;
    i++;
} while (i<5)
```
### for
```js
var sum = 0;
for (var i=0; i<5; i++) {
    sum = sum + i;
}
```
> for에서 continue는 업데이트 구문이 실행되고 조건식을 비교한다
### for in
+ 객체의 각 엘리먼트에 접근할 수 있는 반복문
```js
var property_list = Object.keys(obj);

for (var i=0; i<property_list.length; i++) {
    var propertyName = property_list[i];
    console.log("\t", propertyName, ": ", obj[propertyName]);
} 

for (var propertyName in obj) {
    console.log("\t", propertyName, ": ", obj[propertyName]);
} 
```
> 배열에도 활용 가능. 배열의 인덱스가 변수에 순서대로 저장  
반복문이 아닌 경우 in이 연산자로 동작, 해당 속성의 이름이 객체에 존재하는지 검사, boolean 반환
속성의 이름에 접근하기 전에 in 연산자를 이용해 객체에 해당 속성이 있는지 미리 확인 가능