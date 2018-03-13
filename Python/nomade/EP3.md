List
----
```python
numbers = [1, 3, 5, 7]
numbers
#[1, 3, 5, 7]
3 in numbers
#True
10 in numbers
#False
numbers [-3]
#3
len(numbers)
4
numbers2 = [1, 2, 3, 4, [5, 6, 7], 8, 9, 10]
len(numbers2)
#8
len(numbers2[4])
#3
for i in numbers:
  print(i)
#1
#3
#5
#7
for i in numbers2:
  print(i)
#1
#2
#3
#4
#[5, 6, 7]
#8
#9
#10
numbers
#[1, 3, 5, 7]
```
list 데이터 변경
-------------
```python
numbers = [1, 3, 5, 7, 5]
numbers[0] = 10
numbers.append(9)
numbers.pop(3)
numbers.remove(5)
numbers.insert(1, 11)
#[10, 11, 3, 5, 9]
```
합치기
----
```python
'hello'+'world'
#'helloworld'
['a', 'b'] + ['c', 'd']
['a', 'b', 'c', 'd']
```

슬라이싱
------
```python
numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
numbers[1:]
#[2, 3, 4, 5, 6, 7, 8, 9, 10]
numbers[1:8]
#[2, 3, 4, 5, 6, 7, 8]
numbers[:8]
#[1, 2, 3, 4, 5, 6, 7, 8]
numbers[1:8:2]
#[2, 4, 6, 8]
numbers[1:8:3]
#[2, 5, 8]
numbers[1:8:4]
#[2, 6]
numbers[::2]
#[1, 3, 5, 7, 9]
numbers[::-1]
#[10, 9, 8, 7, 6, 5, 4, 3, 2, 1]
```
