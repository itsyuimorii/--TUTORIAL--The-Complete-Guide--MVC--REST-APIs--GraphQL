## Javascript Refresher

### 1. Introduction
- Javascript is a programming language that is used to make web pages interactive.
- It is a scripting language that is used to create and control dynamic website content, i.e. anything that moves, refreshes, or changes on your screen without requiring you to manually reload a web page.
- It is a client-side programming language that is used to change the behaviour of the web pages.
- It is a lightweight, interpreted programming language.
- It is a prototype-based, multi-paradigm scripting language that is dynamic, and supports object-oriented, imperative, and declarative (e.g. functional programming) styles.

 


### 2. Features
- Javascript is a lightweight, interpreted programming language.
- It is designed for creating network-centric applications.
- It is complementary to and integrated with Java.
- It is an open and cross-platform scripting language.
- It is a client-side scripting language.

### 3. const & let
 | const | let |
|-------|-----|
| const is a signal that the identifier won’t be reassigned. | let is a signal that the variable may be reassigned, such as a counter in a loop, or a value swap in an algorithm. |
| const declaration alone doesn’t really protect your data from being changed. | let declaration alone doesn’t really protect your data from being changed. |
| const is about signaling intent whereas let is about signaling change. | const is about signaling intent whereas let is about signaling change. |
| const is block-scoped. | let is block-scoped. |
| const is not hoisted. | let is not hoisted. |
| const is a constant reference to a value. | let is a mutable reference to a value which can be changed anytime. |
| const is immutable. | let is mutable. |
| const is not immutable objects. | let is not immutable objects. |
| const is not reassignable. | let is reassignable. |
| const is not redeclared. | let is redeclared. |
| const is not reinitialized. | let is reinitialized. |
| const is not temporal dead zone. | let is temporal dead zone. |
 




```javascript
// const
const myName = 'Max';
console.log(myName);

// let
let myName = 'Max';
console.log(myName);

// var
var myName = 'Max';
console.log(myName);
```



### 4. Arrow Functions
- Arrow functions are a new way to write anonymous function expressions.
- Arrow functions are not hoisted.
- Arrow functions always are anonymous.
- Arrow functions do not have their own this. They are not well suited for defining object methods.

```javascript
// ES5
var multiplyES5 = function(x, y) {
  return x * y;
};

// ES6
const multiplyES6 = (x, y) => { return x * y };

// ES6 - concise
const multiplyES6 = (x, y) => x * y;
```


### 5. primitive vs. reference types

<!-- table to introduction those two  -->
 
| Primitive Types | Reference Types |
|-----------------|-----------------|
| Primitive types are stored in the stack. | Reference types are stored in the heap. |
| Primitive types are copied by their value. | Reference types are copied by their reference. |
| Primitive types are independent. | Reference types are dependent. |
| Primitive types are fixed in size. | Reference types are dynamic in size. |
| Primitive types are fast to access. | Reference types are slower to access. |
| Primitive types are destroyed automatically. | Reference types are destroyed by garbage collector. |
| Primitive types are Boolean, Null, Undefined, Number, String, Symbol. | Reference types are Object, Array, Function. |
| Primitive types are immutable. | Reference types are mutable. |
| Primitive types are passed by value. | Reference types are passed by reference. |
| Primitive types are not changeable. | Reference types are changeable. |
| Primitive types are stored in the stack. | Reference types are stored in the heap. |
| Primitive types are copied by their value. | Reference types are copied by their reference. |
| Primitive types are independent. | Reference types are dependent. |
| Primitive types are fixed in size. | Reference types are dynamic in size. |
| Primitive types are fast to access. | Reference types are slower to access. |
| Primitive types are destroyed automatically. | Reference types are destroyed by garbage collector. |
| Primitive types are Boolean, Null, Undefined, Number, String, Symbol. | Reference types are Object, Array, Function. |
| Primitive types are immutable. | Reference types are mutable. |
| Primitive types are passed by value. | Reference types are passed by reference. |
| Primitive types are not changeable. | Reference types are changeable. |
| Primitive types are stored in the stack. | Reference types are stored in the heap. |
| Primitive types are copied by their value. | Reference types are copied by their reference. |
| Primitive types are independent. | Reference types are dependent. |
| Primitive types are fixed in size. | Reference types are dynamic in size. |


```javascript

// Primitive Types
let x = 10;
let y = x;


x = 20;
console.log(x); // 20
console.log(y); // 10

// Reference Types
let x = { value: 10 };
let y = x;

x.value = 20;
console.log(x); // { value: 20 }
console.log(y); // { value: 20 }

```

### 7. Destructuring
