함수
====
####함수 찾는 법
```python
dir(type)
```
####문자열(String)
#####isnumeric()숫자인가?
```python
'1'.isnumeric()
True
'1a'.isnumeric()
False
```
#####title()첫 글자를 대문자로 바꾼다
```python
'abc'.title()
Abc
```
#####upper()대문자로 바꾼다
```python
'abc'.upper()
ABC
```
#####lower()소문자로 바꾼다
```python
'ABC'.lower()
abc
```
####random
#####random.randint(a,b)a부터 b까지의 정수를 랜덤으로 하나 뽑는다
```python
num = random.randint(1,10)
```