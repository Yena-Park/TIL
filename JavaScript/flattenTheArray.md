Given this array:

var myArray = [[1, 2],[3, 4, 5], [6, 7, 8, 9]];   
I want have this result: [1, 2, 3, 4, 5, 6, 7, 8, 9]

Solution 1: Using concat() and apply()
--------------------------------------
```javascript
var myNewArray = [].concat.apply([], myArray);
// [1, 2, 3, 4, 5, 6, 7, 8, 9]
```

Solution 2: Using reduce()
--------------------------
```javascript
var myNewArray = myArray.reduce(function(prev, curr) {
  return prev.concat(curr);
});
// [1, 2, 3, 4, 5, 6, 7, 8, 9]
```

Solution 3:
-----------
```javascript
var myNewArray3 = [];
for (var i = 0; i < myArray.length; ++i) {
  for (var j = 0; j < myArray[i].length; ++j)
    myNewArray3.push(myArray[i][j]);
}
console.log(myNewArray3);
// [1, 2, 3, 4, 5, 6, 7, 8, 9]
```

Solution 4: Using spread operator in ES6
----------------------------------------
```javascript
var myNewArray4 = [].concat(...myArray);
console.log(myNewArray4);
// [1, 2, 3, 4, 5, 6, 7, 8, 9]
```
