```javaScript
//create an array of numbers
var numbers = [1, 2, 3, 4, 5];

//create a variable to hold the sum
var sum = 0;

//Loop over the array, imcrementing the sum variable
numbers.forEach(function(number){
 sum += number;
});

//print the sum variable
sum;
```

```javaScript
//create an array of numbers
var numbers = [1, 2, 3, 4, 5];

//create a variable to hold the sum
var sum = 0;
function adder(number){
 sum += number;
}

//Loop over the array, imcrementing the sum variable
numbers.forEach(adder);

//print the sum variable
sum;
```

Moving Away from For Loops
--------------------------
```javaScript
var posts = [
      { id: 23, title: 'Daily JS News' },
      { id: 52, title: 'Code Refactor City' },
      { id: 105, title: 'The Brightest Ruby' }
    ];
posts.forEach(function(post){
    savePost(post);
});
```

Processing Values
-----------------
```javaScript
var images = [
  { height: 10, width: 30 },
  { height: 20, width: 90 },
  { height: 54, width: 32 }
];
var areas = [];


var images = [
  { height: 10, width: 30 },
  { height: 20, width: 90 },
  { height: 54, width: 32 }
];

var areas = [];

images.forEach(function(image){
    var area = image.height*image.width;
    areas.push(area);
});
areas;
```
.forEach()
==========
* forEach() 메소드는 배열 요소마다 한번씩 제공한 함수를 실행
* Syntax : arr.forEach(callback[, thisArg])
[reference] (https://developer.mozilla.org/ko/docs/Web/JavaScript/Reference/Global_Objects/Array/forEach)
