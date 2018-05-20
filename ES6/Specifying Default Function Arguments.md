```javaScript
function makeAjaxRequest(url, method) {
  if(!method) {
    method = 'GET'; 
  }
  return method;
}

makeAjaxRequest('google.com'); //if you want to pass in a method like undefined or null type, then use null. Null will not try to reassign method to get. But if we passed in undefined then it does get reassigned to GET.
makeAjaxRequest('google.com', 'GET');
```
```javaScript
function makeAjaxRequest(url, method = 'GET') { //if the user didn't not pass in a method argument, then it will automatically reassign method to GET. It is only in the case that we do not provide method as an argument.     
  return method;

}

makeAjaxRequest('google.com'); //output is GET
makeAjaxRequest('google.com', 'POST'); //method will not get reassigned to get. output is POST
```
------------------------------------------------------------------------------------------------------------------------
```javaScript
function User(id){
	this.id = id; 
}

function generateId() {
  return Math.random() * 99999;
}

function createAdminUser(user) {
	user.admin = true;
  
  return user;
}

createAdminUser(new User(generateId()));
```
```javaScript
function User(id){
	this.id = id; 
}

function generateId() {
  return Math.random() * 99999;
}

function createAdminUser(user = new User(generateId())) { //이렇게 하면, whenever I call 'createAdminUser', I can call it just by itself and I get back a random
	user.admin = true;
  
  return user;
}

createAdminUser();
```
Default function parameter(기본 함수 매개변수)
==========================================
* 기본 함수 매개변수를 사용하면 값이 없거나 undefined가 전달된 경우 매개변수를 기본값으로 초기화 할 수 있다.     
  (Default function parameters allow formal parameters to be initialized with default values if no value or <code>undefined</code> is passed.
* JavaScript에서, 함수의 매개변수는 <code>undefined</code>가 기본. 그러나 일부 상황에서는 다른 기본 값을 설정하는 것이 유용할 수 있다. 여기에 기본 매개변수가 도움이 될 수 있다.      
 (In JavaScript, parameters of function s default to <code>undefined</code>. However, in some situations it might be usefuls to set a difference value. This is where default parameters can help)     
[reference](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/Default_parameters)
