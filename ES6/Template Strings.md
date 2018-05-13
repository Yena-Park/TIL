ES5
---
```javaScript
function getMessage() {
 const year = new Date().getFullYear();
 
 return "The year is " + year;
}

getMessage();
```
ES6
---
```javaScript
function getMessage() {
 const year = new Date().getFullYear();
 
 return `The year is ${year}`; //{}안에 수식 넣어도 가능
}

getMessage();
```
```javaScript
function getMessage() {
  return `The year is ${new Date().getFullYear()}`;
}

getMessage();
```

Template literals
=================
* 템플릿 리터럴은 내장된 표현식을 허용하는 문자열 리터럴. 여러줄로 이뤄진 문자열과 문자 보관기능을 사용할 수 있음.
