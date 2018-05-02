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
