연산자
======
### 산술 연산자 (Arithematic operator)
두개의 피연산자(A,b)를 가지는 연산자. `A 연산자 B`  
피연산자는 변수나 숫자도 가능
+ \+ 더하기
+ \- 빼기
+ \* 곱하기
+ \/ 나누기
+ \% 나머지
### 단항 연산자 (Unary operator)
하나의 피연산자(A)를 가지는 연산자. `연산자 A`.  
`-A`로 사용하는 경우는 \-는 이항 연산자가 아닌, 단항 연산자. A변수에 -1을 곱한 효과
#### 증감연산자 (++, --)
표현식 안에서 `변수`의 값을 증가,감소  
`A = A+1, A = A-1`, **연산자를 변수 앞에 사용한 경우와 뒤에 사용한 경우에 따라 변수 값 순서가 바뀐다**
```js
var a;

a = 1;
console.log(++a);
console.log(a);

a = b;
console.log(b++);
console.log(b);

< 2
< 2

< 1
< 2
```
### 관계 연산자 (Relational operator)
두 표현식(A,B)의 관계를 비교하는 이항연산자. 관계에 따라 boolean 타입의 true, false 로 표현

관계연산자 | 동작 | True | False
-----------|------|------|------
< | A보다 B가 더 큰 경우 참 | 3<5 | 3<3
> | A보다 B가 더 작은 경우 참 | 5>3 | 3>3
<= | A보다 B가 크거나 같은 경우 참 | 3<=3 | 4<=3
\>= | A보다 B가 작거나 같은 경우 참 | 3>=3 | 3>=4
== | A와 B가 같은 경우 참 | 3==3 | 4==3
!= | A와 B가 같지 않은 경우 참 | 3!=4 | 3!=3
### 논리 연산자 (Logical operator)
두개의 boolean 피연산자에 대해 논리적으로 연산하는 연산자. 관계에 따라 boolean 타입의 true, false 로 표현
#### AND(&&) 연산자
두 피연산자가 모두 true 인 경우에만 true 를 나타내는 이항연산자

True | False
------|------
True | True | False
False | False | False

#### OR(||) 연산자
두 피연산자가 하나라도 true 인 경우 true 를 나타내는 이항연산자

True | False
------|------
True | True | True
False | True | False

#### NOT(!) 연산자
피연산자가 true 인 경우 false, false 인 경우 true 를 나타내는 단항연산자

### 연산자 우선순위
#### 우선순위 순으로 정리한 연산자
1. ++, --
2. !
3. *, /, %
4. +, -
5. <, <=, >, >=
6. ==, !=
7. &&
8. ||
```js
2 * 3 > 4 + 5 && 6 / 3 == 2 || !false
< 2 * 3 > 4 + 5 && 6 / 3 == 2 || true
< (2*3) > (4 + 5) && (6 / 3) == 2 || true
< (6 > 9) && (2 == 2) || true
< (false && true) || true
< false || true
< true
```
#### 괄호
우선순위를 명시하기 위해 괄호를 사용
+ 부가적 효과
    - 코드의 가독성 향상
    - 연산자 우선순위 실수 방지
    ```js
    height >= 180 && gender == "male" || height >= 165 && gender == "female"
    (height >= 180 && gender == "male") || (height >= 165 && gender == "female")
    ```