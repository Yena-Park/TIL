```javaScript
var computers = [
  { name: 'Apple', ram: 24},
  { name: 'Compaq', ram: 4},
  { name: 'Acer', ram: 32}
];

var allComputersCanRunProgram = true;
var onlySomeComputersCanRunProgram = false;

for (var i = 0; i < computers.length; i++) {
  var computer = computers[i];
  
  if (computer.ram < 16) {
   allComputersCanRunProgram = false; 
  } else {
   onlySomeComputersCanRunProgram = true; 
  }
};

"--------"
allComputersCanRunProgram;
onlySomeComputersCanRunProgram;
```
Every Helper
------------
```javaScript
computers.every(function(computer) {
  return computer.ram > 16; // false(모든 ram이 16이상이 아님)
  return computer.ram > 2; // true(모든 ram은 2이상)
});
```
Some Helper
-----------
```javaScript
computers.some(function(computer) {
  return computer.ram > 16; //true(일부 ram이 16이상암)
});
```
-------------------------------------------------
```javaScript
var names = [
  "Alexandria",
  "Mathew",
  "Joe"
];

names.every(function(name) {
  return name.length > 4;
});

names.some(function(name) {
  return name.length > 4;
});
```
-----------------------------------------
```javaScript
function Field(value) {
 this.value = value; 
}

Field.prototype.validate = function() {
 return this.value.length > 0; 
}

var username = new Field("2cool");
var password = new Field("my_password");
var birthdate = new Field("10/10/2010");

username.validate() && password.validate();

var fields = [username, password, birthdate];

var formIsValidate = fields.every(function(field) {
  return field.validate();
});

if (formIsValid) {
 //allow user to submit 
} else {
 //show an error message
}
```
