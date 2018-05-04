Filtering out with one condition
================================
```javaScript
var products = [
  { name: 'cucumber', type: 'vegetable' },
  { name: 'banana', type: 'fruit' },
  { name: 'celery', type: 'vegetable' },
  { name: 'orange', type: 'fruit' }
];

var filteredProducts = [];

for (var i=0; i<products.length; i++) {
	if (products[i].type === 'fruit') {
    filteredProducts.push(products[i]); 
  }
}
filteredProducts;
```
for 대신에 filter helper 썼을 때
```javaScript
products.filter(function(product) {
  return product.type === 'fruit';
});
```
Filtering out with few conditions
================================
```javaScript
var products = [
  { name: 'cucumber', type: 'vegetable', quantity: 0, price: 1},
  { name: 'banana', type: 'fruit', quantity: 10, price: 15},
  { name: 'celery', type: 'vegetable', quantity: 30, price: 9},
  { name: 'orange', type: 'fruit', quantity: 3, price: 5}
];

//Type is 'vegetable', quantity is greater than 0, price is less than 10

products.filter(function(product) {
 return product.type === 'vegetable' 
   && product.quantity > 0 
   && product.price < 10
});
```
```javaScript
var post = { id: 4, title: 'New Post' };
var comments = [
  { postId: 4, content: 'awesome post'},
  { postId: 3, content: 'it was ok'},
  { postId: 4, content: 'neat'}
];

function commentsForPost(post, comments) {
  return comments.filter(function(comment) {
  return comment.postId === post.id;
  });
}

commentsForPost(post, comments);
```

.filter()
=========
* filter() 메소드는 제공된 함수로 구현된 테스트를 통과하는 모든 요소가 있는 새로운 배열을 만듬.    
* Syntax : var new_array = arr.filter(callback[, thisArg])    
[reference] (https://developer.mozilla.org/ko/docs/Web/JavaScript/Reference/Global_Objects/Array/filter)
