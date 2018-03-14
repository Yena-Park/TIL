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
List Comprehension
------------------
```python
numbers1 = [1, 3, 5, 7]
numbers2 = [2, 4, 6, 8]
i = 0
result = []
for i in range(len(numbers1)):
  result.append(numbers1[i] + numbers2[i])
result
#[3, 7, 11, 15]
```
tuple
-----
```python
numbers = (1, 3, 5, 7, 9)
numbers
#(1, 3, 5, 7, 9)
numbers = 1, 3, 5, 7, 9
numbers
#(1, 3, 5, 7, 9)
```
Packing/Unpacking
-----------------
```python
numbers = (1, 2, 3, 4, 5, 6, 7, 8, 9, 10)
v1, v2, v3, v4 = numbers[-4:]
v1
#7
v2
#8
v3
#9
v4
#10
v1, v2, *others, v9, v10 = numbers
others
#[3, 4, 5, 6, 7, 8]
v1, v2, v3, v4, v5, v6, v7, v8, v9, v10, v11, v12, v13, v14 = (*numbers, 11, 12, 13, 14)
v1, v2, v3, v4, v11, v12, v13, v14
#(1, 2, 3, 4, 11, 12, 13, 14)
x = 1
y = 2
temp = x
x = y
y = temp
print(x, y)
#2 1
x, y = y, x
print(x, y)
#2 1
```
Dict
----
```python
dict_values = {'blue': 10, 'yellow': 3, 'blue': 9, 'red': 7}
10 in dict_values
#False
'blue' in dict_values
#True
for key in dict_values:
    print(key)
#yellow
#blue
#red
for key in dict_values.keys():
    print(key)
#yellow
#blue
#red
for value in dict_values.values():
    print(value)
#3
#9
#7
for (key, value) in dict_values.items():
    print(key, value)
#yellow 3
#blue 9
#red 7
```
