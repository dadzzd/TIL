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
####리스트(List) 다양한 값들을, 순서대로 저장
#####index 리스트의 값에 접근한다
```python
a = [1,2,3,4]
a[0]
a[1]
a[3]
```
#####리스트의 값을 변경한다
```python
a = [1,2,3,4]
a[0] = 5
[5,2,3,4]
```
#####list.append() 리스트를 추가 한다
```python
a = [1,2,3]
a.append(4)
a
[1,2,3,4,]
```
#####list.del 리스트의 값을 제거 한다
```python
a = [1,2,3,4]
del a[0]
2,3,4
```
#####list.slice(start, end, step) 리스트의 값을 선택해서 자른다
```python
a = [1,2,3,4]
a[slice(1,3)]
[2,3]
a[slice(1,10,3)] = a=[1:10:3]
a[:] == a[slice(None, None)]
```
####딕셔너리(dict) 다양한 값들을 key:value 사전 형태 저장하는 구조
```python
{ 'name':'sol', 'phone':'010-1234-1234'}
dict(name='sol', phone='010-1234-1234'}
```
#####dict[key] 딕셔너리의 값에 접근한다
```python
dict[name]
```
#####del dict[key] 딕셔너리의 값을 제거한다
```python
dek dict[name]
```