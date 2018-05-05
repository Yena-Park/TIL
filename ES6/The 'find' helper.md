Find an object in an array by one of its properties
----------------------------------------------------
```javaScript
var users = [
  { name: 'Jill' },
  { name: 'Alex' },
  { name: 'Bill'}
];

var user;

for (var i=0; i<users.length; i++){
  if(users[i].name === 'Alex') {
   user = users[i]; 
   break;
  }
};

user;
```
for loop 대신에 find helper 사용
```javaScript
var users = [
  { name: 'Jill' },
  { name: 'Alex' },
  { name: 'Bill'}
];

users.find(function(user) {
  return user.name === 'Alex';
});
```
----------------------------------------
```javaScript
function Car(model) {
  this.model = model;
};

var cars = [
  new Car('Buick'),
  new Car('Camero'),
  new Car('Focus')
];

cars.find(function(car) {
  return car.model === 'Focus';
});
```
------------------------------------------
```javaScript
var posts = [
  { id: 1, title: 'New Post'},
  { id: 2, title: 'Old Post'}
];

var comment = {postId:1, content: 'Great Post'};

function postForComment(posts, comment) {
  return posts.find(function(post) {
    return post.id === comment.postId;
  });
};

postForComment(posts, comment);
```
Finding admin users
-------------------
```javaScript
var users = [
  { id: 1, admin: false },
  { id: 2, admin: false },
  { id: 3, admin: true }
];

var admin = users.find(function(user){
   return user.admin === true; 
});

admin;
```
Finding a balance
-----------------
```javaScript
var accounts = [
  { balance: -10 },
  { balance: 12 },
  { balance: 0 }
];

var account = accounts.find(function(account){
    return account.balance == 12;
});

account;
```

.find()
=======
* find() 메서드는 해당 배열 안의 값을 하나(첫번째) 반환. 이 때, 콜백으로 전달받은 테스트 함수가 요구하는 조건을 만족하는 값을 반환. 그렇지 않으면 undefined를 반환.
* Syntax: arr.find(callback[, thisArg])
  * callback: 배열의 각 값에 대해서 실행시킬 함수.
  * array: find 함수의 대상이 되는 배열.
  * thisArg: 선택항목, 콜백이 호출될 때 <code>this</code>로 사용될 객체

[reference](https://developer.mozilla.org/ko/docs/Web/JavaScript/Reference/Global_Objects/Array/find)
