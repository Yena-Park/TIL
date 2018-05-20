Rest operator(...)
-------------
```javaScript
function addNumbers(numbers){
  return numbers.reduce((sum, number) =>{
    return sum+number;
  }, 0); 
}

addNumbers([1, 2, 3, 4, 5]); //output is 15
```
I want to pass in a bunch of numbers not it array.
```javaScript
function addNumbers(...numbers){ //It means that I don't know how many numbers are(howewver many there will some snumber of arguments). I want to capture all of those arguments and put them into a single array
 
  return numbers.reduce((sum, number) =>{
    return sum+number;
  }, 0); 
}

addNumbers(1, 2, 3, 4, 5, 6, 7); //output is 28
```
Spread Operator
---------------
```javaScript
const defaultColors = ['red', 'green'];
const userFavoriteColors = ['orange', 'yellow'];

defaultColors.cancat(userFavoriteColors); //output is ["red","green","orange","yellow"]
```javaScript
const defaultColors = ['red', 'green'];
const userFavoriteColors = ['orange', 'yellow'];

[...defaultColors, ...userFavoriteColors]; //[this is that new array] we just generated a completely new one. Then inside of it we referenced an existing array and infront of it put a dot dot dot. So this what we refer to this as the dot dot dot as the spread operator.
```
-----------------------------------------------------------------------------------------------------------------------------------------
```javaScript
function validateShoppingList(...items) {
  if(items.indexOf('milk') < 0) {
    return ['milk', ...items];
  }
  return items;
}

validateShoppingList('orange', 'bread', 'eggs'); //output is ["milk","orange","bread","eggs"]
```
Rest Operator
=============
* Rest operator is used to kind of gather together variables.     
[reference](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/rest_parameters)

Spread Operator
===============
* Spread operator is used to kind of flatten or spread them out.     
[reference](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Spread_syntax)
