```javaScript
var name = 'Jane';
var title = 'Software engineer';
var hourlyWage = 40;

//ES6
const name = 'Jane';

let title = 'Software engineer;
let hourlyWage = 40;

title = 'Senior Software Engineer';
hourlyWage = 45;
```
Why we need to use const/let?
-----------------------------
```javaScript
function count(targetString) {
	var characters = ['a', 'e', 'i', 'o', 'u'];
	var number = 0;
  
  for (var i=0; i < targetString.length; i++) {
   if(characters.includes(targetString[i])) {
    number++; 
   }
  }
   return number;
}

count('aeiobzxceiaipbiox');
```
```javaScript
function count(targetString) {
	const characters = ['a', 'e', 'i', 'o', 'u']; //const로 해두면 누구나 처음에 이 코드를 봐도, 앞으로 Character 라는 변수가 바뀌지 않는다는 걸 알수 있다.
	let number = 0; //number는 바뀔꺼라는걸 예상할 수 있다.   more instantly readable 하게 만들어줌.
  
  for (var i=0; i < targetString.length; i++) {
   if(characters.includes(targetString[i])) {
    number++; 
   }
  }
   return number;
}

count('aeiobzxceiaipbiox');
```

Const / Let
==========
* const : 읽기 전용 참조를 생성. 상수 초기자(initializer)가 필요. 변수 재선언과 재할당 모두 불가능
  [reference] (https://developer.mozilla.org/ko/docs/Web/JavaScript/Reference/Statements/const)
* let : 블록 유효 범위를 갖는 지역 변수를 서언하며, 선언과 동시에 임의의 값으로 초기화할 수도 있음. 변수에 재할당 가능
  [reference] (https://developer.mozilla.org/ko/docs/Web/JavaScript/Reference/Statements/let)
  
What's difference between var, let and const
===========================================
 > var : function-scoped
 > let, const : block-scoped
```javaScript
// let
let a = 'test'
let a = 'test2' // Uncaught SyntaxError: Identifier 'a' has already been declared
a = 'test3'     // 가능

// const
const b = 'test'
const b = 'test2' // Uncaught SyntaxError: Identifier 'a' has already been declared
```
b = 'test3'    // Uncaught TypeError:Assignment to constant variable.</code>
