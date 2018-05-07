Sum all the values of an array
------------------------------
```javaScript
var numbers = [10, 20, 30];
var sum = 0;

for (var i = 0; i < numbers.length; i++) {
  sum += numbers[i];
};
```
for loop 대신 reduce helper 사용
```javaScript
var numbers = [10, 20, 30];

numbers.reduce(function(sum, number) {
  return sum+number;
}, 0);
```
--------------------------------------------------------
```javaScript
var primaryColors = [
  { color: 'red'},
  { color: 'yellow'},
  { color: 'blue'}
];

primaryColors.reduce(function(previous, primaryColor) {
  previous.push(primaryColor.color);
  
  return previous;
}, []);
```
------------------------------------------------------------
```javaScript
function balancedParens (string) {
  return string.split("").reduce(function(previous, char) {
    if (previous < 0) { return previous; }
    if (char === "(") { return ++previous; }
    if (char === ")") { return --previous; }
    return previous;
  }, 0);
}

balancedParens("(((("); //결과는 4

```

.reduce()
=========
* reduce() 메서드는 왼쪽에서 오른쪽으로 이동하며 배열의 각 요소마다 누적 계산값과 함께 함수를 적용해 하나의 값으로 줄임.
* Syntax: arr.reduce(callback[, initialValue])
