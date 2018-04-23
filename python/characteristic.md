특징
====
#### 대문자와 소문자를 구분
##### 거북이 그래픽 모듈
    1960년대 Logo라는 프로그래밍 언어의 일부로 개발된 컴퓨터 그래픽 방식
    shape(모양)
        t.shape("classic"), t.shape("trutle"), t.shape("triangle")
    forward(거리) -> fd: 전진
    left(각도) -> lt: 왼쪽 회전
    right(각도) -> rt: 오른쪽 회전
    circle(반지름) : 원 그리기
    down() / pendown() : 꼬리 내리기
    up() / penup() : 꼬리 올리기
    speed(속도) : 거북이 속도
        t.speed(1) : 가장 느린 속도, t.speed(10) : 빠른 속도, t.speed(0) : 최고 속도
    color(색 이름) : 색상 바꾸기
    bgcolor(색 이름) : 배경색 바꾸기
    fillcolor(색 이름) : 도형 내부 색 바꾸기
    begin_fill() : 도형 내부 색칠 준비
    end_fill() : 도형 내부 색칠
    showturtle() / st() : 거북이를 화면에 표시
    hidentrutle() / ht() : 거북이를 화면에서 숨김
    clear() : 거북이를 둔 채 화면을 지움
    reset() : 화면을 지우고 거북이도 원래 자리와 상태로 되돌림
    pensize : 굵기
     ```python
     import turtle as t
     t.forward(50)
     t.right(90)
     ```
#### 연산
##### 더하기 
```python
7+4
11
```
##### 빼기
        ```python
        7-4
        3
        ```
    * 곱하기
        ```python
        7*4
        28
        ```
    * 나누기
        ```python
        7/4
        1.75
        ```
    * 제곱(같은 수를 여러 번 곱함)
        ```python
        2**3
        2를 세 번 곱함 8
        ```
    * 정수로 나누었을 때의 몫
        ```python
        7//4
        1(나눗셈의 몫)
        ```
    * 정수로 나누었을 때의 나머지
        ```python
        7%4
        3
        ```
    * 다른 계산보다 괄호 안을 먼저 계산
        ```python
        2*(3+4)
        14
        ```
    * 파이썬에서는 중괄호나 대괄호를 사용하지 않고 소괄호 여러 개를 사용해서 표현한다
        ```python
        5+(4*(3+(1+2)))
        29
        ```
* 변수
    * 변수 이름은 영문 대/소문자, 숫자, 밑줄(_)로만 만들 수 있다. 공백 사용 불가
    * 영문 대/소문자를 구분
    * 변수 이름은 숫자로 시작할 수 없다.
    * 파이썬 문법으로 사용하는 단어는 사용할 수 없다.
        * False, None, True, and, as, assert, break, class, continue, def, del, elif, else, except, finally, for, from, global, in, is, lambda, nonlocal, not, or, pass, raise, return, try, while, with, yield 등