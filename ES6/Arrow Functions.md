ES5
---
```javaScript
const add = function(a, b) {
  return a + b;
}
add(1, 2);
```
ES6
---
1. funtion을 지우고, argument 뒤에 => 넣어준다.
2. return 을 지우고, {}를 지운다.
3. 만약 argument가 하나라면, () 역시 생략 가능하다.
```javaScript
const add = (a, b) => a + b;
add(1, 2);
```
1
----
```javaScript
const team = {
  members: ['Jane', 'Bill'],
  teamName: 'Super Squad',
  teamSummary: function() {
   return this.members.map(function(member){
     return `${member} is on team ${this.teamName}`;
   }.bind(this));
  }
};

team.teamSummary();
```
2
---
```javaScript
const team = {
  members: ['Jane', 'Bill'],
  teamName: 'Super Squad',
  teamSummary: function() {
   	var self = this;
    return this.members.map(function(member){
     return `${member} is on team ${self.teamName}`;
   });
  }
};

team.teamSummary();
```
3
---
```javaScript
const team = {
  members: ['Jane', 'Bill'],
  teamName: 'Super Squad',
  teamSummary: function() {
   return this.members.map((member) => {
     return `${member} is on team ${this.teamName}`;
   });
  }
};

team.teamSummary();
```

Arrow Function Expression
=========================
* function 표현에 비해 구문이 짧고 자신의 this, arguments, super 또는 new,target을 바인딩 하지 않는다. 화살표 함수는 항상 익명이다. 이 함수 표현은 메소드 함수가 아닌 곳에 가장 적당하다. 그래서 생성자로서 사용할 수 없다.     
[reference](https://developer.mozilla.org/ko/docs/Web/JavaScript/Reference/Functions/%EC%95%A0%EB%A1%9C%EC%9A%B0_%ED%8E%91%EC%85%98)
