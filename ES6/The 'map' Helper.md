Mapping an array of numbers to an array of multiplication by 2
==============================================================
```javaScript
var numbers = [1, 2, 3];
var doubledNumbers = [];

var doubled = numbers.map(function(number){
  return number * 2;
});

doubled;
```

Using map to reformat objects in an array
=========================================
```javaScript
var  cars = [
  { model: 'Buick', price : 'CHEAP'}, 
  { model: 'Camaro', price: 'expensive'}
];

var prices = cars.map(function(car) {
  return car.price;
});

prices;
```
```javaScript
var trips = [
  { distance: 34, time: 10 },
  { distance: 90, time: 50 },
  { distance: 59, time: 25 }
];

var speeds = trips.map(function(trip){
   return trip.distance / trip.time;
});

speeds;
```
.map()
======
* Syntax : var new_array = arr.map(function callback(currentValue[, index[, array]])
* map() 메소드는 배열내의 모든 요소 각각에 대하여 제공된 함수(callback)를 호출하고, 그 결과를 모아서, 새로운 배열을 반환    
> 예시 : 숫자의 배열을 받아 각 숫자들의 제곱근이 들어있는 새로운 배열 만들기    
> <code> var numbers = [1, 4, 9]; </code>    
> <code> var roots = numbers.map(Math.sqrt); </code>    
> <code> //roots의 값은 [1, 2, 3]이 되지만, numbers는 그대로 [1, 4, 9] </code>    

[reference] (https://developer.mozilla.org/ko/docs/Web/JavaScript/Reference/Global_Objects/Array/map)
