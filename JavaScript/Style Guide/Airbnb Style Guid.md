# Airbnb JavaScript Style Guid(){

*A mostly reasonable approach to Javascript*

## Table of Contents

  1. [Types](#types)
  1. [Objects](#objects)
  1. [Arrays](#arrays)
  1. [Strings](#strings)
  1. [Functions](#functions)
  1. [Properties](#properties)
  1. [Variables](#variables)
  1. [Hoisting](#hoisting)
  1. [Comparison Operators & Equality](#comparison-operators--equality)
  1. [Blocks](#blocks)
  1. [Comments](#comments)
  1. [Whitespace](#whitespace)
  1. [Commas](#commas)
  1. [Semicolons](#semicolons)
  1. [Type Casting & Coercion](#type-casting--coercion)
  1. [Naming Conventions](#naming-conventions)
  1. [Accessors](#accessors)
  1. [Constructors](#constructors)
  1. [Events](#events)
  1. [Modules](#modules)
  1. [jQuery](#jquery)
  1. [ECMAScript 5 Compatibility](#ecmascript-5-compatibility)
  1. [Testing](#testing)
  1. [Performance](#performance)
  1. [Resources](#resources)
  1. [In the Wild](#in-the-wild)
  1. [Translation](#translation)
  1. [The JavaScript Style Guide Guide](#the-javascript-style-guide-guide)
  1. [Chat With Us About Javascript](#chat-with-us-about-javascript)
  1. [Contributors](#contributors)
  1. [License](#license)

## Types
 - **Primitives**: When you access a primitive type you work directly on its value.   
   + `string`
   + `number`
   + `boolean`
   + `null`
   + `undefined`
   
   ```javascript
   var foo = 1;
   var bar = foo;
   
   bar = 9;
   
   console.log(foo, bar); // => 1, 9
   ```
 - **Complex**:When you access a complex type you work on a reference to its value.
   + `object`
   + `array`
   + `function`
   
   ```javascript
   var foo = [1, 2];
   var bar = foo;
   
   bar[0] = 9;
   
   console.log(foo[0], bar[0]); // => 9, 9
   ```
## Objects
 - Use the literal syntax for object creation.
   ```javascript
   //bad
   var item = new Object();
   
   //good
   var item = {};
   ```
 - Don't use reserved words as keys.
   ```javascript
   //bad
   var superman = {
    default: {clark: 'kent'},
    private: true
   };
   
   //good
   var superman = {
    defaults: {clark: 'kent'},
    hidden: ture
   };
   ```
 - Use readable synonyms in place of reserved words.
   ```javascript
   //bad
   var superman = {
    class: 'alien'
   };
   
   //bad
   var superman = {
    klass: 'alien'
   };
   
   //good
   var superman = {
    type: 'alien'
   };
   ```
}

## Arrays
 - Use the literal syntax for array creation.
   ```javascript
   //bad
   var items = new Array();
   
   //good
   var items = [];
   ```
 - Use Array#push instead of direct assignment to add items to an array.
   ```javascript
   var someStack = [];
   
   //bad
   someStack[somStack.length] = 'abracadabra';
   
   //good
   someStack.push('abracadabra');
   ```

 - When you need to copy an array use Array#slice. [jsPerf](http://jsperf.com/converting-arguments-to-an-array/7)
   ```javascript
   var len = item.length;
   var itemsCopy = [];
   var i;
   
   //bad
   for(i = 0; i < len; i++) {
    itemsCopy[i] = items[i];
   }
   
   //good
   itemsCopy = items.slice();
   ```
 - To convert an array-like object to an array, use Array#slice.
   ```javascript
   function trigger() {
     var args = Array.prototype.slice.call(arguments);
   }
   ```
## Strings
 - Use single quotes `''` for strings.
   ```javascript
   //bad
   var name = "Bob Parr";
   
   //good
   var name = 'Bob Parr';
   
   //bad
   var fullName = "Bob " + this.lastName;
   
   //good
   var fullname = 'Bob ' + this.lastName;
   ```
   
 - Strings longer than 1-- characters should be written across multiple lines using string concatenation.
 - Note: If overused, long strings with concatenation could impact performance.
   ```javascript
   //bad
   var errorMessage = 'This is a super long error that was thrown because of Batman. When you stop to think about how Batman had anything to do with this, you would get nowhere fast.';
   
   //bad
   var errorMessage = 'This is a super long error that was thrown because \
    of Batman. When you stop to think about how Batman had anything to do \
    with this, you would get nowhere \
    fast.';
   
   //good
   var errorMessage = 'This is a super long error that was thrown because ' +
   'of Batman. When you stop to think about how Batman had anything to do ' +
   'with this, you would get nowhere fast.';
   ```
 - When programmatically building up a string, use Array#join instead of string concatenation. Mostly for IE:
   ```javascript
   var items;
   var messages;
   var length;
   var i;
   
   message = [{
    state: 'success',
    message: 'This one worked.'
    }, {
    state: 'success',
    message: 'This one worked as well.'
    }, {
    state: 'error',
    message: 'This one did not work.'
   }];
   
   length = messages.length;
   
   //bad
   function inbox(messages) {
    items = '<ul>';
    
    for (i = 0; i < length; i++ ) {
      items += '<li>' + messages[i].message + '</li>';
    }
    return items + '</ul>';
   }
   
   //good
   function inbox(messages) {
    items = [];
    
    for (i = 0; i < length; i++) {
      //use direct assignment in this case because we're micro-optimizing.
      items[i] = '<li>' + messages[i].message + '</li>';
    }
    
    return '<ul>' + items.join('') + '</ul>';
   }
   ```
## Functions
 - Function expressions:
   ```javascript
   //anonymous function expression
   var anonymouns = function () {
    return true;
   };
   
   //named function expression
   var named = function named() {
    return true;
   };
   
   //imediately-invoked function expression (IIFE)
   function () {
    console.log('Welcom to the Internet. Please follow me.');
   }
   ```
 - Never declare a function in a non-vumcion block (if, while, etc). Assign the function to a variable instead. Browsers will aloow you to do it, but they all interpret it differently, which is bad news bears.
 - **Note:** ECMA-262 defines a `block` as a list of statements. Afunction declaration is not a statement. 
   ```javascript
   //bad
   if (currentUser) {
    function test() {
      console.log('/Nope.');
    }
   }
   
   //good
   var test;
   if (currentUser) {
    test = function test() {
      console.log('Yup');
    };
   }
   ```
 - Never name a parameter `arguments`. This will take precedence over the `arguments` object that is given to every function scope.
   ```javscript
   //bad
   function npope(name, options, arguments) {
    // ...stuff...
   }
   
   //good
   function yup(name, options, args) {
    // ...stuff...
   }
   ```

## Properties
 - Use dot notation when accessing properties.
   ```javascript
   var luke = {
    jedi: true,
    age: 28
   };
   
   //bad
   var isJedi = luke['jedi'];
   
   //good
   var isJedi = luke.jedi;
   ```
 - Use subscript notation `[]` when accessing properties with a variable.
   ```javascript
   var luke = {
    jedi: true,
    age: 28
   };
   
   function getProp(prop) {
    return luke[prop];
   }
   
   var isJedi = getProp('jedi');
   ```
## Variables

  - Always use `var` to declare variables. Not doing so will result in global variables. We want to avoid polluting the global namespace. Captain Planet warned us of that.

    ```javascript
    // bad
    superPower = new SuperPower();

    // good
    var superPower = new SuperPower();
    ```

  - Use one `var` declaration per variable.
    It's easier to add new variable declarations this way, and you never have
    to worry about swapping out a `;` for a `,` or introducing punctuation-only
    diffs.

    ```javascript
    // bad
    var items = getItems(),
        goSportsTeam = true,
        dragonball = 'z';

    // bad
    // (compare to above, and try to spot the mistake)
    var items = getItems(),
        goSportsTeam = true;
        dragonball = 'z';

    // good
    var items = getItems();
    var goSportsTeam = true;
    var dragonball = 'z';
    ```

  - Declare unassigned variables last. This is helpful when later on you might need to assign a variable depending on one of the previous assigned variables.

    ```javascript
    // bad
    var i, len, dragonball,
        items = getItems(),
        goSportsTeam = true;

    // bad
    var i;
    var items = getItems();
    var dragonball;
    var goSportsTeam = true;
    var len;

    // good
    var items = getItems();
    var goSportsTeam = true;
    var dragonball;
    var length;
    var i;
    ```

  - Assign variables at the top of their scope. This helps avoid issues with variable declaration and assignment hoisting related issues.

    ```javascript
    // bad
    function () {
      test();
      console.log('doing stuff..');

      //..other stuff..

      var name = getName();

      if (name === 'test') {
        return false;
      }

      return name;
    }

    // good
    function () {
      var name = getName();

      test();
      console.log('doing stuff..');

      //..other stuff..

      if (name === 'test') {
        return false;
      }

      return name;
    }

    // bad - unnecessary function call
    function () {
      var name = getName();

      if (!arguments.length) {
        return false;
      }

      this.setFirstName(name);

      return true;
    }

    // good
    function () {
      var name;

      if (!arguments.length) {
        return false;
      }

      name = getName();
      this.setFirstName(name);

      return true;
    }
    ```
