# Airbnb JavaScript Style Guid(){

* A mostly reasonable approach to Javascript

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
   
## Object
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
