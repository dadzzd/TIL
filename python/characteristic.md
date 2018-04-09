특징
====
* 대문자와 소문자를 구분
* 거북이 그래픽 모듈
    * forward -> fd: 전진
    * left -> lt: 왼쪽 회전
    * right -> rt: 오른쪽 회전
    * color : 색상
    * pensize : 굵기
     ```python
     import turtle as t
     t.forward(50)
     t.right(90)
     ```
* 연산
    * 더하기 
        ```python
        7+4
        11
        ```
    * 빼기
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