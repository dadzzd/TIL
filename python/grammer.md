문법
====
#### 반복문
* for문
    * 들여쓰기 된 부분을 열 번 반복
    ```python
    for x in range(10):
        print("Hello!")
    ```
    * 파이썬에선 네 칸 띄어쓰기를 추천
* range란?
    * range는 범위를 뜻한다.
    * 파이썬에서는 range는 반복할 '범위'를 지정하는 명령어
    * range(5) : 0부터 시작해서 4까지 다섯 번 반복한다(5는 제외)
    * range(1,11) : 1부터 시작해서 10까지 열 번 반복한다(11은 제외)
    ```python
    list(range(5))
    [0,1,2,3,4]
    list(range(0,5))
    [0,1,2,3,4]
    list(range(1,11))
    [1,2,3,4,5,6,7,8,9,10]
    list(range(1,4))
    [1,2,3]
    ```
* 입출력
    * input
    ```python
    name = input("Your name? ")
    print("Hello", name)
    Your name? 김길벗
    Hello 김길벗
    ```
* 자료형
    
    | 자료형 | 영어이름 | 파이썬 표기 | 설명 | 예 |
    |--------|----------|-------------|------|----|
    | 정수   | integer  | int         | 소수점이 없는 수 | -2,-1,0,1,2,3 |
    | 소수   | Floating-point number | float | 소수점(.)이 있는 수, 부동소수점수라고도 불린다 | -3.5, 0.0, 1.25, 5.0 |
    | 문자열 | String | str | 알파벳 혹은 다른 문자로 이루어진 문장 | "a", "abc", "Hello?", "3 people", "비", "여름" |