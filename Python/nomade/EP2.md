```python
name = "Hellp, Python"
birth = 1990
age = 2017 - birth
print(name, age)
##Hello, Python 27
name2 = "Yena Park"
birth2 = 1989
age2 = 2018 - birth2
print(name2, birth2, age2)
print(name2, birth2, age2)
#Yena Park 1989 29
```
몫과 나머지
--------
```python
10 / 3
#3.3333333333333335
10 // 3
#3
10 % 3
#1
```

사칙연산
------
```python
2 + 3
#5
3 - 10
#-7
3 * 10
#30
3 / 10
#0.3
3 // 10
#0
10 % 3
#1
10 ** 3
#1000
2 ** 1000
#10715086071862673209484250490600018105614048117055336074437503883703510511249361224931983788156958581275946729175531468251871452856923140435984577574698574803934567774824230985421074605062371141877954182153046474983581941267398767559165543946077062914571196477686542167660429831652624386837205668069376
```

Boolean Type
------------
```python
a = []
b = []
id(a), id(b)
#(4401949448, 4401972488)
a == b
#True
a is b
#False
c = b
id(a), id(b), id(c)
#(4401949448, 4401972488, 4401972488)
b is c
#True
True and False #true && false
#False
True or False #true || false
#True
not True #!true
#False
3 > 10
#Flase
10 >= 10
#True
```

String Type
-----------
```python
name1 = 'Python'
name2 = 'Python'
name1 == name2
#True
name1
#'Python'
name2
#'Python'
'I\'m Tom'
#"I'm Tom"
print('I\'m Tom')
#I'm Tom
```
여러줄 문자열
----------
```python
lyrics = '''The now glows white on the mountain tonight
Now a footprint to b e seen A kingdom of isolation
and it looks like I'm the queen'''
print(lyrics)
#The now glows white on the mountain tonight
#Now a footprint to b e seen A kingdom of isolation
#and it looks like I'm the queen
```
format 함수
----------
```python
print('{0}, {1}, {2}'. format('a', 'b', 'c'))
#a, b, c
print('{}, {}, {}'. format('a', 'b', 'c'))
#a, b, c
print('{2}, {1}, {0}'. format('a', 'b', 'c'))
#c, b, a
print('{2}, {1}, {0}'. format(*'abc'))
#c, b, a
print('{1}, {1}, {0}'. format('a', 'b', 'c'))
#b, b, a
print('Coordinates: {lat}, {lng}'. format(lat='37.24N', lng='-115.81W'))
#Coordinates: 37.24N, -115.81W
coord = {'lat': '37.24N', 'lng': '-115.81W'}
print('Coordinates: {lat}, {lng}'. format(**coord))
#Coordinates: 37.24N, -115.81W
score = 80
if score > 100:
    print('you are good')
    yena = 'babo'
if score == 80:
    print('hi')
    yena = 'beautiful'
    print(yena)
#hi
#beautiful
print(yena)
#beautiful
```
